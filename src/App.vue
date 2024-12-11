<template>
  <MyHeader appName="BOOK HAVEN"/> 
  <BooksList :books=books />
  <MyFooter />
</template>

<script>
import MyHeader from './components/MyHeader.vue';
import BooksList from './components/BooksList.vue';
import MyFooter from './components/MyFooter.vue';


export default{
  name: 'App',
  components:{
    MyHeader,
    BooksList,
    MyFooter
  },
  data(){
    return {
      books: []
    }
  },
  methods:{
    async fetchBooks(){
      const res = await fetch('https://bookshavennode.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data.books;
    }
  },
  async created(){
      this.books = await this.fetchBooks();
  }
}
</script>


<style>

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: sans-serif;
}

#app{
  background-color: #c9d3ee;
}
</style>
