<template>
  <nav>
        <RouterLink class="link" to="/">Home</RouterLink>
        <RouterLink class="link" to="/colunas">Colunas</RouterLink>
      </nav>
</template>

<script>
import {RouterLink} from 'vue-router'
export default {
    components:{
        RouterLink
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