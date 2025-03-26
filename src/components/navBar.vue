<template>
  <nav>
        <RouterLink v-show= "home" class="link" to="/">Home</RouterLink>
        <RouterLink v-show= "colunas" class="link" to="/colunas">Colunas</RouterLink>
        <RouterLink v-show = "curio" class="link" to="/curiosidades">Curiosidades</RouterLink>
      </nav>
</template>

<script>
import {RouterLink} from 'vue-router'
export default {
    components:{
        RouterLink
    },
    props: {
        home: Boolean,
        colunas: Boolean,
        curio: Boolean,

    }
}
</script>

<style scoped>
nav{
    background-color: var(--cor1);
    padding: 10px;
    display: flex;
    justify-content: space-between;
}

.link {
    text-decoration: none;
    color: var(--cor2);
    transition: 0.5s;

}

.link:hover {
    background-color: var(--cor2);
    color: var(--cor1);

}

</style>