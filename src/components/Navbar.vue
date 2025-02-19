<script setup>
import { ref } from 'vue'

const selectedLanguage = ref('en') // Default language
const cost = ref(0.00);

const languages = [
  { code: 'en', name: 'English' },
  { code: 'fr', name: 'French' },
  { code: 'es', name: 'Spanish' }
]
</script>

<template>
  <nav class="navbar navbar-expand-lg navbar-light sticky-top white-bg">
    <div class="container d-flex flex-column gap-4">
      <div class="d-flex justify-content-between align-items-center w-100">
        <router-link to="/" class="navbar-brand">
        <img src="/public/images/menu-logo.png" alt="logo" class="img-fluid">
      </router-link>
      <div class="d-flex gap-2">
        <div>
          <select id="lang" v-model="selectedLanguage" class="btn btn-primary">
            <option v-for="lang in languages" :key="lang.code" :value="lang.code">
              {{ lang.name }}
            </option>
          </select>
        </div>
        <div>
          <button class="btn btn-secondary d-flex align-items-center gap-1" type="button" data-bs-toggle="offcanvas"
            data-bs-target="#offcanvasExample" aria-controls="offcanvasExample">
            <img src="/public/images/cart.svg" alt="cart" width="14" height="14">
            {{ cost }}
          </button>

          <div class="offcanvas offcanvas-end" tabindex="-1" id="offcanvasExample"
            aria-labelledby="offcanvasExampleLabel">
            <div class="offcanvas-header">
              <h5 class="offcanvas-title" id="offcanvasExampleLabel">Offcanvas</h5>
              <button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas"
                aria-label="Close"></button>
            </div>
            <div class="offcanvas-body">
              <!-- <div>
                Some text as placeholder. In real life you can have the elements you have chosen. Like, text, images, lists, etc.
              </div> -->
              <div class="dropdown mt-3">
                <button class="btn btn-secondary dropdown-toggle" type="button" id="dropdownMenuButton"
                  data-bs-toggle="dropdown">
                  Dropdown button
                </button>
                <ul class="dropdown-menu" aria-labelledby="dropdownMenuButton">
                  <li><a class="dropdown-item" href="#">Action</a></li>
                  <li><a class="dropdown-item" href="#">Another action</a></li>
                  <li><a class="dropdown-item" href="#">Something else here</a></li>
                </ul>
              </div>
            </div>
          </div>
        </div>
      </div>
      </div>
      <div class="w-100 position-relative">
        <span class="search-icon">
          <i class="fa-solid fa-magnifying-glass"></i>
        </span>
        <input type="search" name="search" id="serach" class="form-control search-input" placeholder="Search">
      </div>
    </div>
  </nav>
</template>

<style scoped>
.navbar-brand {
  width: 120px;
  height: auto;
}

select, button {
  font-size: 14px;
  height: 32px;
  font-weight: 500;
}

.search-input{
  background-color: rgb(239 240 246 / var(--tw-bg-opacity, 1));
  border: none;
  padding-left: 40px;
}

.search-input::placeholder{
  font-size: 14px;
  font-weight: 400;
}

.search-icon{
  position: absolute;
  left: 20px;
  top: 50%;
  transform: translate(-50%, -50%);
  font-size: 14px;
}
</style>