<template>
    <navbar />
    <main-categories />
</template>

<script>
import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'
import MainCategories from '../components/home/MainCategories.vue'

export default {
    name: 'home',
  components: {
    Navbar,
    MainCategories,
    RouterLink,
    RouterView
  }
}
</script>