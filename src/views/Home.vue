<template>
  <div class="container">
      <x-card v-for="todo of filteredTodo" :key="todo.id" >
          <h1>{{todo.title}}</h1>
          <p></p>
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
           todos: [],
        }
    },
    computed:{
        filteredTodo(){
            return this.todos.filter(todo => todo.completed);
        }

    },
    methods: {
        getTodos() {
             axios.get('/todos').then(response => {
                 this.todos = response.data;
            })
        }
    },
    mounted() {
        this.getTodos();
    }
}
</script>

<style scoped>
    h1 {
        font-weight: 400;
        color: #2c2a2a;
        font-size: 15px;
        text-transform: capitalize;
    }
</style>