<template>
  <div id="book">
    <h3>{{ book.title }}</h3>
    <img :src='book.img_url'>
    <p>By: {{ book.author }}</p>
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
