<template>
  <nav>
      <router-link :to="{name: 'Home'}">Home</router-link>
      <router-link :to="{name: 'About'}">About</router-link>
  </nav>
</template>

<script>
export default {

}
</script>

<style scoped>
nav {
   background: #000; 
   padding: 14px;
}
nav a {
    margin-left: 10px;
    color: #fff;
    text-decoration: none;
    padding: 14px;
}
.router-link-active {
    background: red;
}
</style>