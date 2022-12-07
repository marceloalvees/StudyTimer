<template>
  <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
    </div>
    <div class="column is-three-quarter">
      <BarraLateral/>
    </div>
  </main>
</template>

<script lang="ts">
import { defineComponent } from 'vue';
import BarraLateral from './components/BarraLateral.vue';

export default defineComponent({
    name: "App",
    components: { BarraLateral }
});
</script>

<style>

</style>
