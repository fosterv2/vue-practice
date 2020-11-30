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
  data () {
    return {
      title: 'The Name of the Wind',
      img_url: 'https://images-na.ssl-images-amazon.com/images/I/51JThzjy3gL._SX306_BO1,204,203,200_.jpg',
      author: 'Patrick Rothfuss'
    }
  }
}
</script>
