<template>
 <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateral></BarraLateral>
    </div>
     <div class="column is-three-quarter">
       <VueFormulario/>
     </div>
 </main>
</template>

<script lang="ts">

import {defineComponent} from "vue";
import BarraLateral from "@/components/BarraLateral.vue";
import VueFormulario from "@/components/VueFormulario.vue";

export default defineComponent({
  name: 'App',
  components: {VueFormulario, BarraLateral}
})
</script>

<style>

</style>
