<script setup>
import nonVeg from '@/assets/images/non-veg.png';
</script>

<template>
    <div class="d-flex gap-3">
        <div class="sub-cate d-flex justify-content-center align-items-center px-3 py-1">
            <img :src="nonVeg" alt="non veg" class="img-fluid">
            <p>non-veg</p>
        </div>
        <div class="sub-cate d-flex justify-content-center align-items-center px-3 py-1">
            <img :src="nonVeg" alt="non veg" class="img-fluid">
            <p>non-veg</p>
        </div>
    </div>
</template>

<style scoped>
.sub-cate{
    background-color: rgb(239 240 246 / var(--tw-bg-opacity, 1));
    border-radius: 1.5rem;
    width: max-content;
}
.sub-cate p{
    font-size: 14px;
    font-weight: 500;
}
</style>