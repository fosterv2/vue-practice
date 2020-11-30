<template>
  <div id="app">
    <!-- <img src="./assets/logo.png"> -->
    <!-- <Book :title='title' :img_url='img_url' :author='author' /> -->
    <Book
      v-for='book in books'
      :key='book.id'
      :book='book'
    />
    <router-view/>
  </div>
</template>

<script>
import Book from './components/Book'

export default {
  name: 'App',
  components: {
    Book
  },
  data () {
    return {
      books: [
        // {
        //   id: 0,
        //   title: 'The Name of the Wind',
        //   img_url: 'https://images-na.ssl-images-amazon.com/images/I/51JThzjy3gL._SX306_BO1,204,203,200_.jpg',
        //   author: 'Patrick Rothfuss'
        // }
      ]
    }
  },
  mounted: function () {
    fetch('http://localhost:3000/books')
      .then(resp => resp.json())
      .then(books => {
        this.books = books
      })
  }
}

// const getBooks = () => {
//   fetch('http://localhost:3000/books')
//     .then(resp => resp.json())
//     .then(books => {
//       this.books = books
//     })
// }
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
