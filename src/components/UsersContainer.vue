<template>
  <main>
    <h1 v-if="isLoading">Cargando...</h1>
    <user v-else :user="user" v-for="(user, index) in users" :key="index"/>
  </main>
</template>

<script>
import User from '@/components/User';
import axios from 'axios';

export default {
  data() {
    return {
      users: [],
      isLoading: true
    };
  },
  components: {
    User
  },
  created(){
    axios.get('http://localhost:5000/users')
      .then(response => {
        this.users = response.data;
      })
      .catch(err => console.error(err))
      .finally(() => {
        this.isLoading=false;
      });
  }
};
</script>
