<template>
  <div>

    <main id="main">
      <service></service>
      <about></about>
      <action></action>
      <focus></focus>
      <feature></feature>
      <produits></produits>
      <contact></contact>
      
    </main>
    <!-- End #main -->
  </div>
</template>

<script>
import service from '../components/sections/services.vue'
import about from '../components/sections/about.vue'
import action from '../components/sections/action.vue'
import focus from '../components/sections/focus.vue'
import feature from '../components/sections/features.vue'
import produits from './sections/produits.vue'
import contact from '../components/sections/contact.vue'

export default {
  name: "HelloWorld",
  components : {
    contact,
    service,
    about,
    action,
    focus,
    feature,
    produits
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
</style>
