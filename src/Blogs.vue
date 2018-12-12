<template>
    <div class="blogs">
        <button @click="loaadData">Load data</button>
        <button @click="deleteData">Del data</button>
        <div v-for="post in posts" :key="post.id" class="blogs_items" :id="'post'+post.id">
            <h1 class="blogs_items_title">{{post.title}}</h1>
            <p class="blogs_items_text"> {{post.body}}</p>
        </div>
    </div>
</template>

<script>
    import axios from  'axios'
  export default {
    data () {
      return {
        posts: [],
      }
    },
    created () {

    },
    methods: {
      loaadData () {
        axios.get('https://jsonplaceholder.typicode.com/posts/')
          .then(response => {
            this.posts = response.data;
          }).catch(error => {
          console.error(error);
        })
      },
      deleteData () {
        this.posts = [];
      },
    },

  }
</script>

<style scoped>

</style>