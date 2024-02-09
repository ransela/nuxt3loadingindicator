<template>
  <div>
    <h1>Page 1</h1>
    <button @click="navigate()">Navigate to page 2</button>
  </div>
</template>

<script setup>
async function navigate() {
  navigateTo('/second');
}
</script>
