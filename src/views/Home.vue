<template>
    <navbar />
    <main-categories />
</template>

<script setup>
// import { ref } from 'vue'
import { RouterLink, RouterView } from 'vue-router'
import Navbar from '../components/Navbar.vue'
import MainCategories from '../components/home/MainCategories.vue'
</script>