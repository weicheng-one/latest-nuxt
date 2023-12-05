<script setup>
const { find } = useStrapi();

const response = await find("posts");
</script>
<template>
  <div>
    <NuxtWelcome />
    {{ response }}
  </div>
</template>
