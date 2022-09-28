<template>
 <main class="columns is-gapless is-multiline">
    <div class="column is-one-quarter">
      <BarraLateral></BarraLateral>
    </div>
     <div class="column is-three-quarter">
       <VueFormulario/>
       <div class="lista">
         <TaskAction/>
       </div>
     </div>
 </main>
</template>

<script lang="ts">

import {defineComponent} from "vue";
import BarraLateral from "@/components/BarraLateral.vue";
import VueFormulario from "@/components/VueFormulario.vue";
import TaskAction from "@/components/TaskAction.vue";

export default defineComponent({
  name: 'App',
  components: {TaskAction, VueFormulario, BarraLateral}
})
</script>

<style>
.lista {
  padding: 1.5rem;
}
</style>
