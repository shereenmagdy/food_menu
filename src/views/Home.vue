<template>
    <navbar />
</template>

<script>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'

export default {
    name: 'home',
  components: {
    Navbar,
    RouterLink,
    RouterView
  }
}
</script>