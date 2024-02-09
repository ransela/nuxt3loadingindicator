<template>
  <div>test</div>
</template>

<script setup>
// Set the layout
definePageMeta({
  layout: 'other',
});

const { data, pending, error, refresh } = await useAsyncData('mountains', () =>
  stall(5000)
);

async function stall(stallTime = 3000) {
  await new Promise((resolve) => setTimeout(resolve, stallTime));
}
</script>
