<template>
    <navbar />
    <main-categories />
    <sub-categories />
</template>

<script setup>
// import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'
import MainCategories from '../components/home/MainCategories.vue'
import subCategories from '../components/home/subCategories.vue'
</script>