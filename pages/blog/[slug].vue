<script setup lang="ts">
import { useRoute } from 'vue-router'

const route = useRoute()
const post = await queryCollection('content').path(route.path).first()
</script>

<template>
  <div v-if="post">
    <h1>{{ post.title }}</h1>
    <div v-html="post.body"></div>
  </div>
  <div v-else>
    <p>Post not found.</p>
  </div>
</template>
