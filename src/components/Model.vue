<script setup lang="ts">
import { useGLTF } from '@tresjs/cientos'

const { state } = await useGLTF('/models/Four_stroke_public_7.glb')
const scene = state.value!.scene
</script>

<template>
  <primitive :object="scene" />
</template>