<script setup>
const route = useRoute();
const { data: post } = await useAsyncData(() =>
  queryContent("posts").where({ slug: route.params.slug }).findOne()
);
</script>

<template>
  <div v-if="post">
    <h1>{{ post.title }}</h1>
    <img :src="post.image" alt="Post Image" />
    <p>{{ post.date }}</p>
    <div v-html="post.body"></div>
  </div>
</template>
