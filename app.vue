<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup>

useHead({
  script: [
    { src: "https://identity.netlify.com/v1/netlify-identity-widget.js" },
  ],
});

</script>