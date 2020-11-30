<template>
  <div class="book">
    <h3>{{ book.name }}</h3>
    <img :src='book.img_url'>
    <p>By: {{ book.author_name }}</p>
  </div>
</template>

<script>
export default {
  name: 'Book',
  // props: {
  //   title: String,
  //   img_url: String,
  //   author: String
  // }
  props: {
    book: Object
  }
}
</script>

<style>

</style>
