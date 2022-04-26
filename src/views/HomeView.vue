<template>
  <div class="home">
    <Header></Header>
    <HelloWorld/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Header from '../components/Header.vue'

export default {
  name: 'HomeView',
  components: {
    HelloWorld,
    Header,
  }
}
</script>
