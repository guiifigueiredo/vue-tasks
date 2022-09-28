<template>
  <div
      class="is-flex is-align-items-center is-justify-content-space-between"
  >
    <StopWatch :tempo="tempo"/>
    <ButtonAction @buttonClick="iniciar" texto="play" icone="fas fa-play" :desabilitado="isActive"/>
    <ButtonAction @buttonClick="finalizar" icone="fas fa-stop" texto="stop" :desabilitado="!isActive"/>
  </div>
</template>

<script>
import { defineComponent } from "vue";
import StopWatch from "@/components/StopWatch";
import ButtonAction from "@/components/ButtonAction";

export default defineComponent({
  name: 'TimerBreak',
  emits: [
      'breakTime'
  ],
  components: {
    ButtonAction,
    StopWatch
  },
  data() {
    return {
      tempo : 0 ,
      cronometro : 0 ,
      isActive: false
    }
  },
  methods: {
    iniciar(){
      this.isActive = true
      this.cronometro = setInterval(() => {
        this.tempo += 1
      }, 1000)
      console.log('iniciado ')
    },
    finalizar(){
      this.isActive = false
      clearInterval(this.cronometro)
     this.$emit('breakTime', this.tempo)
      this.tempo = 0
      console.log('finalizado')
    }
  }
})
</script>

<style scoped>

</style>
