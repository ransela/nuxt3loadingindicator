<template>
  <div>test</div>
</template>

<script setup>
// Set the layout
definePageMeta({
  layout: 'other',
});

const { data, pending, error, refresh } = await useAsyncData('mountainssss', () =>
  stall(3000)
);

async function stall(stallTime = 3000) {
  await new Promise((resolve) => setTimeout(resolve, stallTime));
}
</script>
