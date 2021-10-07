<template>
  <div class="block-head" :style="`background-color: ${blockProps.headColor}`"></div>
</template>

<script>
export default {
  name: 'BlockHead',
  props: ['blockProps']
}
</script>

