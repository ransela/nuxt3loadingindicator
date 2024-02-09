<template>
  <div>
    <NuxtLayout class="layouts">
      <div v-show="show">
        <NuxtLoadingIndicator color="#fed250" :height="15" />
      </div>
      <NuxtPage />
    </NuxtLayout>
  </div>
</template>



<script setup>
const nuxtApp = useNuxtApp();
const show = ref(false);

addRouteMiddleware('global-loader', () => show.value = true, { global: true })
nuxtApp.hook('page:finish', () => show.value = false)
</script>