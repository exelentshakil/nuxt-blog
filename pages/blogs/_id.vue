<template>
  <div class="container">
      <div class="post">
        <h1>{{ blog.title }}</h1>
        <p>{{ blog.body }}</p>
      </div>
  </div>
</template>

<script>
import axios from 'axios'

export default {
    data() {
        return {
            blog: {}
        }
    },
    methods: {
       async fetchBlog() {
            const req = await axios.get('https://jsonplaceholder.typicode.com/posts/' + this.$route.params.id);
            const data = await req.data;
            this.blog = data;
        }
    },
    mounted(){
        this.fetchBlog()
    }
}
</script>

<style scoped>
  .container {
    margin: 0 auto;
  }
  .post {
    display: flex;
    flex-direction: row;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    height: 60vh;
    background-color: #eceaea85;
    margin: 0 auto;
    padding: 100px;
  }

  .post h1{
    font-size:40px;
    font-weight:900;
    line-height: 1.2;
  }
  .post p {
    font-size:16px;
    font-weight: 500;
  }

</style>
