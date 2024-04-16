<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/LSPD.png"/>

    <h1><RouterLink to="/">LSPD BBCode Formatter</RouterLink></h1>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  text-align: center;
}

.logo {
  width: 250px;
  padding-bottom: 2rem;
}

h1 {
  padding-bottom: 3rem;
}

@media only screen and (min-width: 768px) {
  header {
    text-align: initial;
  }

  .logo {
    float: right;
  }
}
</style>
