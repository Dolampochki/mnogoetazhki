<template>
  <div class="block-body">
    <BlockBodyFloor v-for="floorNum in blockProps.floorsCount * 1" :key="floorNum" :blockProps="blockProps" :floorNum="floorNum" :blockNum="blockNum" :blockSide="blockSide"></BlockBodyFloor>
  </div>
</template>

<script>
import BlockBodyFloor from '@/components/BlockBodyFloor.vue'
export default {
  name: 'BlockBody',
  props: ['blockProps', 'blockNum', 'blockSide'],
  components: {
    BlockBodyFloor
  }
}
</script>

