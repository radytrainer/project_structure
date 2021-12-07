<template>
  <div class="container">
     <x-card v-for="user of users" :key="user.id">
      <u>
        <li>{{ user.name }}</li>
        <li>{{ user.email }}</li>
        <li>{{ user.address.city }}</li>
      </u>
     </x-card>
  </div>
</template>

<script>
import Card from "../components/ui/Card.vue";
import axios from '../axios-http.js';
export default {
    components: {
        'x-card': Card
    },
    data() {
        return {
           users: [],
        }
    },
   
    methods: {
        getUsers() {
             axios.get('/users').then(response => {
                 this.users = response.data;
            })
        }
    },
    mounted() {
        this.getUsers();
    }
}
</script>

<style>

</style>