<template>
    <header>
        <h1>
            <img src="../assets/Logo.png" alt="">
        </h1>
    </header>
</template>
<script lang="ts">
import { defineComponent } from 'vue';

export default defineComponent({
    name:'SideBar'
})
</script>
<style scoped>
header{
    background: #0d3b66;
    width: 100%;
    height: 100vh;
}

img{
        padding-left: 25px;
        padding-right: 25px;
    }
@media only screen and (max-width: 768px){
    header {
        padding: 2.5rem;
        height: auto;
    }
}
</style>
