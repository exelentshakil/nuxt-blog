<template>
    <div class="container">
      <div class="menu">
        <ul id="nav">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/about">About</NuxtLink></li>
          <li><NuxtLink to="/blog">Blog</NuxtLink></li>
          <li><NuxtLink to="/contact">Contact</NuxtLink></li>
        </ul>
        </div>
    </div>
</template>

<style scoped>
  .menu {
      justify-content: center;
      display: flex;
      padding: 20px 27px;
      background-color: rgba(168, 25, 25, 0.856);
  }

  ul#nav li {
      display: inline-block;
      color:#fff;
  }


  ul#nav li a:hover {
      background: rgba(168, 25, 25, 0.856);
      padding: 10px 27px;
      color: #fff;
  }

  ul#nav li a {
      padding: 10px 27px;
  }
</style>