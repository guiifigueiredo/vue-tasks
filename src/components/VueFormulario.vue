<template>
  <div class="box">
    <div class="columns">
      <div
          class="column is-8"
          role="form"
          aria-label="Formulário para criação de uma nova tarefa"
      >
        <input
            type="text"
            class="input"
            placeholder="Qual tarefa você deseja iniciar?"
            v-model="descricao"
        />
      </div>
      <div class="column">
        <TimerBreak @breakTime="finalizarTarefa"/>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
  import { defineComponent } from "vue";
  import StopWatch from "@/components/StopWatch.vue";
  import TimerBreak from "@/components/TimerBreak.vue";

  export default defineComponent({
    name: 'VueFormulario',
    components: {
      TimerBreak
    },
    data(){
      return {
        descricao: ''
      }
    },
    methods: {
      finalizarTarefa(tempoDecorrido: number) : void {
        console.log('tempo da tarefa', tempoDecorrido)
        console.log('descricao:', this.descricao)

        this.descricao = ''
      }
    }
  })
</script>

<style scoped>

</style>
