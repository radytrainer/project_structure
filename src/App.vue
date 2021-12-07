<template>
  <main>
    <navbar></navbar>
    <router-view/>
  </main>
</template>

<script>
import Navbar from './components/navbar/Navbar.vue'

export default {
 components: {
   'navbar': Navbar,
 }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
  font-family: sans-serif;
}
.container {
  width: 80%;
  margin: 0 auto;
}
</style>
