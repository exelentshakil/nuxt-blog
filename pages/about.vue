<template>
  <div class="container">
      <div class="home">
        <h1>About</h1>
        <p>Your way to the moon!</p>
      </div>
  </div>
</template>

<script>
export default {
    head: {
      title: 'About',
      meta: [
        { charset: 'utf-8' },
        { name: 'viewport', content: 'width=device-width, initial-scale=1' },
        {
          hid: 'description',
          name: 'description',
          content: 'Your way to the moon!'
        }
      ],
    }
}
</script>

<style scoped>
  .container {
    margin: 0 auto;
  }
  .home {
    display:flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    height: 100vh;
    background-color: #eceaea85;
    margin:0 auto;
  }

  .home h1{
    font-size:60px;
    font-weight:900;
  }
  .home p {
    font-size:16px;
    font-weight: 500;
  }

</style>
