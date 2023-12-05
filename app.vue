<script setup>
const { find } = useStrapi();

const { data, error } = await useAsyncData("posts", () => find("posts"));
</script>
<template>
  <div>
    <NuxtWelcome />
    <pre>{{ data }}</pre>
    <pre>{{ error }}</pre>
  </div>
</template>
