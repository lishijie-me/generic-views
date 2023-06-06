<template>
  <div class="home">
    <img alt="my logo" src="../assets/logo.png">
    <HelloWorld msg="Welcome to my Generic Views"/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld
  }
}
</script>
