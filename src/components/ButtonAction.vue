<template>
  <button class="button" @click="buttonClick" :disabled="desabilitado">
            <span class="icon">
              <i :class="icone"></i>
            </span>
    <span>{{texto}}</span>
  </button>
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: 'ButtonAction',
  emits: [
    'buttonClick'
  ],
  props: {
    desabilitado: {
      type: Boolean
    },
    texto: {
      type: String ,
      required: true
    },
    icone: {
      type: String ,
      required: true
    }
  },
  methods: {
    buttonClick() : void {
      this.$emit('buttonClick')
    }
  }
})
</script>

<style scoped>

</style>
