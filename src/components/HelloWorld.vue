<script setup lang="ts">
import {TresCanvas} from '@tresjs/core'
import { OrbitControls } from '@tresjs/cientos'
function pointermove(i,p) {
  console.log(i, p);
}

</script>

<template>
  <TresCanvas ref="tresCanvasRef" window-size clear-color="#82DBC5">
    <TresPerspectiveCamera :args="[45, 1, 0.1, 1000]"  />
    <OrbitControls  :enableDamping="true"/>
    <TresMesh @click="pointermove">
      <TresTorusGeometry :args="[1, 0.5, 16, 32]" />
      <TresMeshBasicMaterial color="orange" />
    </TresMesh>
    <TresAmbientLight :intensity="1" />
  </TresCanvas>
</template>

<style scoped></style>
