<template>
  <section class="library">
      <BooksList v-bind:books="books" />
  </section>
</template>

<script>
import books from './assets/childrensbooks.json';
import BooksList from './views/books';

export default {
    components: {
        BooksList
    },
    computed: {
        books() {
            return books.books;
        }
    }
}
</script>

<style>
    @import url('https://fonts.googleapis.com/css?family=Roboto:400,900&display=swap');

    body {
        margin: 0;
    }

    .library {
        height: 100vh;
        display: flex;
        justify-content: center;
        align-items: center;
        -webkit-font-smoothing: antialiased;
        -moz-osx-font-smoothing: grayscale;
        font-family: 'Roboto', sans-serif;
    }
</style>