<template>
  <section id="curiosidades">
    <NavBar 
    :home="nav.home" 
    :colunas="nav.colunas"
    :curio="nav.curio"
    
    />
    <article>
      <div class="molduraAnimada" @click="defCor">
      <img src="/img/girassol-vanGoh.jpg" alt="O quadro girrasois de Vicent Van GoH, girassois em uma vaso" id="girassol-vanGoh">
      </div>
      <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit. Pariatur quam nobis quibusdam doloribus quas molestias deserunt ipsam eius a culpa consectetur dignissimos id maxime, repellendus reiciendis earum, hic tempore, labore saepe fugiat. Facere possimus ullam cupiditate placeat earum veniam ipsum temporibus, hic sequi sapiente, libero iure maxime, corporis perspiciatis vitae aliquid minus provident nulla eligendi nobis nemo. Dolorem, perspiciatis sint.</p>
      <p>{{ cor }}</p>
    </article>
    <article>
      <div class="molduraAnimada">
      
      </div>
    </article>
    
  </section>
</template>

<script>
import NavBar from '@/components/navBar.vue';

export default {
  components:{
    NavBar
  },

  data(){
   return{
      nav:{
        home: true,
        curio: false,
        colunas: true
      },
      cor: Number,
    }
  },
  methods:{
   GerarCor(){
    this.cor = Math.floor(Math.random()* 5 + 1)
    Math.floor(this.cor)
    console.log(this.cor)
   },

   defCor(){
    setInterval(this.GerarCor, 1000)
   }

  },
  mounted(){
    this.defCo
  }
}

</script>

<style>

article{
  display:flex;
  columns: 2;
  margin: 10px auto;
  padding: 10px;
}

.molduraAnimada{
  background-color: aquamarine;
  widows: 250px;
  padding: 10px;
}

#girassol-vanGoh{
  width: 200px;
}

p {
  margin: 15px 20px;
  max-width: 750px;
}

</style>