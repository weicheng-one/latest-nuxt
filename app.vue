<script setup>
const { find } = useStrapi();

const { data, pending, refresh, error } = await useAsyncData("posts", () =>
  find("posts")
);
</script>
<template>
  <div>
    <NuxtWelcome />
    <pre>{{ data }}</pre>
    <pre>{{ pending }}</pre>
    <pre>{{ error.message }}</pre>
  </div>
</template>
