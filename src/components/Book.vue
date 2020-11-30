<template>
  <div id="book">
    <h3>{{ title }}</h3>
    <img :src='img_url'>
    <p>By: {{ author }}</p>
  </div>
</template>

<script>
export default {
  name: 'Book',
  props: {
    title: String,
    img_url: String,
    author: String
  }
}
</script>
