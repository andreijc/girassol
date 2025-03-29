<template>
  <section id="curiosidades">
    <NavBar 
    :home="nav.home" 
    :colunas="nav.colunas"
    :curio="nav.curio"
    
    />
    <article>
      <div class="molduraAnimada"
      :style="{backgroundColor: cor
      }"
       >
      
      <img src="/img/girassol-vanGoh.jpg" alt="O quadro girrasois de Vicent Van GoH, girassois em uma vaso" id="girassol-vanGoh">
      </div>
      <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit. Iure sunt neque nihil sed eaque. Quo quisquam accusantium cum facere veniam voluptas dolorum corrupti unde nisi eaque incidunt, obcaecati nostrum aspernatur!</p>
      
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
      cores:[
            'var(--cor1)',
            'var(--cor2)',
            'var(--cor3)',
            'var(--cor4)',
            'var(--cor5)',],
      cor: String,
      index: Number,
    }
  },
  methods:{
   gerarCor(){
   this.cor = this.cores[Math.floor(Math.random()* this.cores.length)]
   },

   defCor(){
    setInterval(this.gerarCor, 2000)
   }

  },
  mounted(){
    this.defCor()
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
  transition: 1.5s background-color ease;
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