<template>
    <div>
      <nav>
        <button role="button" @click="openMenu(true)" v-if="!isMenuOpen">
          Open Menu
        </button>
        <button role="button" @click="openMenu(false)" v-else>
          Close Menu
        </button>
        <ul v-if="isMenuOpen">
          <li>
            <a href="/">Home</a>
          </li>
          <li>
            <a href="/about">About</a>
          </li>
        </ul>
      </nav>
    </div>
  </template>
  
  <script setup>
  import { ref } from 'vue';
  
  const isMenuOpen = ref(false)
  
  const openMenu = (action) => {
    isMenuOpen.value = action;
  }
  </script>