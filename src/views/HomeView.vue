<template>
  <headerImg />
  <NavBar
    :home="nav.home" 
    :colunas="nav.colunas"
    :curio="nav.curio"
    />
  <div id="icon-girassol">
        <img  :class="{giro: status_giro}" @click="gira" src="/img/icone-girasssol.png" alt="Um girassol">
  </div>
<main>
  <article :class="{letraentra: status_letra}">
    <h2>Titulo 1</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium magni, nisi dolorem nulla unde sit minima blanditiis odio eum? Saepe architecto temporibus dolore velit unde nesciunt magnam illo, labore, quae quis voluptatem fugit. Animi unde blanditiis ipsam molestiae aut voluptas.</p>
  </article>
  
  <article :class="{letraentra: status_letra}">
    <h2>Titulo 2</h2>
    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ipsa quas aliquid ea asperiores quae harum deleniti placeat ipsum commodi, doloribus esse, adipisci corrupti possimus error sequi, quibusdam nisi eius quia.</p>
  </article>
</main>

</template>

<script>
import NavBar from '../components/navBar.vue';
import HeaderImg from '../components/headerImg.vue'


export default {
  components:{
    NavBar,
    HeaderImg,
  },

  data() {
    return {
      status_giro: false,
      status_letra: false,
      nav: {
        home: false,
        colunas: true,
        curio: true
      }
    }
    
  },

  methods: {
    gira(){
      this.status_giro = true
      setTimeout(()=>{this.status_giro = false}, 1000)
    },

    entra(){
      this.status_letra = true
      setTimeout(()=>{this.status_letra = false}, 850)
    }
  },
  mounted(){
    this.gira()
    this.entra()
  }
}
</script>

<style scoped>
#icon-girassol{
  background-color: var(--cor1);
  width: 100px;
  height: 100px;
  padding: 4px;
  border-radius: 50%;
  margin: auto;
  margin-top: -65px;
  display: block;
}

.giro {
  animation: giro 1s linear infinite
}


main {
  display: flex;
  gap: 40px;
}

.letraentra {
  animation: letraentra 0.85s linear infinite;
}

h1 {
  text-align: center;
}

p {
  margin: 15px;
  line-height: 1.5em;
  text-align: justify;
  text-indent: 30px;
}

@keyframes giro {
  0% {
    transform: rotate(0deg) scale(1);
  }

  50% {
    transform: rotate(180deg) scale(1.1);
  }

  100% {
    transform: rotate(360deg) scale(1);
  }
}

@keyframes letraentra {
  0% {
    opacity: 0;
    transform: translateY(80px);
  }

  100%{
    opacity: 1;
    transform: translateY(0);

  }
}

</style>