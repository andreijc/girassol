<template>
  <section>
    <NavBar
    :home="nav.home" 
    :colunas="nav.colunas"
    :curio="nav.curio"
    />

  </section>
</template>
<script>
import NavBar from '@/components/navBar.vue';


export default {
  components: {
    NavBar
  },

  data(){
    return{
      nav: {
        home: true,
        culunas: false,
        curio: true
      }
    }
  }
}
</script>
<style>

</style>
