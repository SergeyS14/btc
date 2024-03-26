<script setup>
  import Header from './components/header.vue' 
  import Main from './components/Main.vue'
  import Support from './components/support.vue'
</script>

<template>
  <div class="bg-image">
    <Header/>
    <Main/>
  </div>
    <Support/>
</template>

<style scoped>


.bg-image{
    background: url("./assets/images/Rectangle.png");
    margin: 0;
    padding: 0;
    width: 100%;
    height: 100%;
}

</style>
