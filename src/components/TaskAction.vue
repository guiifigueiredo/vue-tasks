<template>
<div class="box has-text-weight-bold">
  <div class="columns">
    <div class="column is-7">
      Descrição da tarefa
    </div>
    <div class="column">
      <StopWatch/>
    </div>
  </div>
</div>
</template>

<script lang="ts">
import {defineComponent} from "vue";
import StopWatch from "@/components/StopWatch.vue";

export default defineComponent({
  name: "TaskAction",
  components: {StopWatch}
})
</script>

<style scoped>
.box {
  background-color: #FAF0CA;
}
</style>
