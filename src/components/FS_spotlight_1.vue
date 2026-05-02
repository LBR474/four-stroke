<script setup lang="ts">
import { TresCanvas } from '@tresjs/core'
import { OrbitControls, useGLTF } from '@tresjs/cientos'
import Model from './Model.vue';
</script>

<template>
  <TresCanvas clear-color="#111" window-size>
    <TresPerspectiveCamera :position="[0, 1, 5]" />

    <OrbitControls />

    <Suspense>
      <Model />
    </Suspense>

    <TresAmbientLight :intensity="1.5" />
    <TresDirectionalLight :position="[3, 3, 3]" :intensity="2" />
  </TresCanvas>
</template>