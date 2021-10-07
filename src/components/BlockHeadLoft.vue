<template>
  <div class="block-head-loft">
    <div class="block-head-loft-item left edge" :style="`background-color: ${blockProps.headColor}`"></div>
    <div class="block-head-loft-item center" :style="`background-color: ${blockProps.headColor}`"></div>
    <div class="block-head-loft-item right edge" :style="`background-color: ${blockProps.headColor}`"></div>
  </div>
</template>

<script>
export default {
  name: 'BlockHeadLoft',
  props: ['blockProps'],
}
</script>

