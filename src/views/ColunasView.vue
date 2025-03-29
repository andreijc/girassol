<template>
<<<<<<< HEAD
  <div class="about">
      </div>
</template>
=======
  <section>
    <NavBar
    :home="nav.home" 
    :colunas="nav.colunas"
    :curio="nav.curio"
    />
>>>>>>> home

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
