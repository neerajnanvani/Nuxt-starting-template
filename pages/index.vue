<template>
  Hello from Index

  <div v-show="base">heyyyyyyyyy</div>
</template>

<script setup>
const base = ref(false);

useHead({
  title: 'HomePage',
});

let i = 0;

onMounted(() => {
  while (i < 100000) {
    i = i + 1;
  }

  base.value = true;
});
</script>
