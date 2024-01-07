<script setup>
import './assets/app.css'
import Wedding from './components/Wedding.vue'
import Items from './components/Items.vue'

import { ref } from 'vue';

// Create a ref for the List component
const listRef = ref(null);

// Function to call the toggleDetails method in List component
const toggleListDetails = () => {
  listRef.value.toggleDetails();
};
</script>

<template>
  <div id="title-box">
    <Wedding text="Wedding List" />
  </div>
  <div style="margin-left: 50px;">
    <Items ref="listRef" />
  </div>
  
  <div style="display: flex; justify-content: center; text-align: center;">
    <button @click="toggleListDetails" id="button">Show/Hide Details</button>
  </div>
</template>