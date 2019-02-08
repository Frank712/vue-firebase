<template>
  <div id="app" class="main">
    <span>{{ title }}</span>
    <entrance />
  </div>
</template>

<script>
  import Entrance from '@/views/Entrance.vue';

  export default {
      name: 'App',
      components: { Entrance },
      data() {
          return {
              title: 'Entrances'
          }
      }
  }
</script>

<style>
  html {
    font-size: 62.5%;
  }
  .main {
    background-color: #a21010;
    padding: 10px;
    color: white;
    border-radius: 5px;
    width: 400px;
    font-size: 3rem;
    text-align: center;
  }

  a {
    text-decoration: none;
    color: #553f75;
  }

  button {
    background-color: #553f75;
    color: white;
    font-size: 2.4rem;
    font-weight: bold;
    border-style: none;
    border-radius: 5px;
    padding: 3px 10px;
    margin: 3px 5px;
    min-width: 35px;
    cursor: pointer;
  }

</style>