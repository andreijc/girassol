<template>
  <headerImg />
  <div id="icon-girassol">
        <img src="/img/icone-girasssol.png" alt="Um girassol">
      </div>
<main>
  <article>
    <h2>Titulo 1</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Praesentium magni, nisi dolorem nulla unde sit minima blanditiis odio eum? Saepe architecto temporibus dolore velit unde nesciunt magnam illo, labore, quae quis voluptatem fugit. Animi unde blanditiis ipsam molestiae aut voluptas.</p>
  </article>
  
  <article>
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

main {
  display: flex;
  gap: 40px;
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

</style>