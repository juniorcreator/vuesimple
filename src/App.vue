<template>
  <div id="app" class="wrapper">
    <div class="container">
      <h1>Main component </h1>
      <blogs></blogs>
    </div>
  </div>
</template>

<script>
  import blogs from "./Blogs.vue"
export default {
  name: 'app',
  data () {
    return {

    }
  },
  created () {

  },
  methods: {

  },
  components: {
    blogs: blogs,
  },
}
</script>

<style lang="scss" scoped>
  html, body {
    height: 100%;
  }

</style>
