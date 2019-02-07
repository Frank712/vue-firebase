<template>
  <div id="app" class="main">
    <span>App Vue-Firebase</span>
    <entrance />
    <client/>
  </div>
</template>

<script>
  import Entrance from '@/views/Entrance.vue';
  import Client from '@/components/Client.vue';

  export default {
      name: 'App',
      components: { Entrance, Client },
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

</style>