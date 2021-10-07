<template>
  <ul class="block-footer" :style="`background-color: ${blockProps.brickColor}`">
    <li v-for="brickRow in 5" :key="brickRow">
      <ul class="brick-row">
        <li class="brick" v-for="brick in 68" :key="brick"></li>
      </ul>
    </li>
  </ul>
</template>

<script>
export default {
  name: 'BlockFooter',
  props: ['blockProps'],
}
</script>

