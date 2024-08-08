<template>
  <div>
    <div ref="aRef">被拖拽的整个区域
      <div ref="bRef">用来操作拖拽的区域，可以是aRef</div>
    </div>
  </div>
</template>
<script setup lang="ts">
const aRef = ref(null)//被拖拽的整个区域
const bRef = ref(null) //用来操作拖拽的区域，可以是aRef
const draggable = ref(true) // 是否可拖拽
const overflow = ref(true) // 是否可拖出可视区域
import { useDraggable } from './use-draggable';
useDraggable(aRef, bRef, draggable, overflow)
</script>