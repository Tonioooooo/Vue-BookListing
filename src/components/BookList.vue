<template>
  <div>
    <h1>{{title}}</h1>
    <ul>
      <book-item v-for="book in books" :book='book' :key='book.id'></book-item>
    </ul>
  </div>
</template>

<script>
import BookItem from "./BookItem";
export default {
  name: "BookList",
  components: { BookItem },
  data() {
    return {
      title: "All Books",
      books: [
        { id:0, title: "Self-Reliance", author: "Ralph Waldo Emerson" },
        { id:1, title: "American Gods", author: "Neil Gaiman" },
        { id:2, title: "Amusing Ourselves to Death", author: "Neil Postman" }
      ]
    };
  }
};
</script>

<style>
h1,
h2 {
  font-weight: normal;
}

ul {
  list-style-type: none;
  padding: 0;
}
</style>
