<template>
  <header>
    <headerImg />
    <navBarVue />
  </header>

  <RouterView />
</template>
<script>
import { RouterView } from 'vue-router'
import navBarVue from './components/navBar.vue'
import headerImg from './components/headerImg.vue'

export default {
  components: {
    RouterView,
    navBarVue,
    headerImg
  }
}
</script>

<style>
:root {
  --cor1: #4F7302;
  --cor2: #D9A404;
  --cor3: #D98E04;
  --cor4: #BF5B04;
  --cor5: #732C02;
}

* {
  margin: 0;
  padding: 0;
  font-family: Arial, Helvetica, sans-serif;
}

</style>
