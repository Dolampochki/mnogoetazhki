<template>
  <div div class="block-body-floor" :class="`floor-${floorNum}`">
    <BlockBodyItem v-for="itemNum in 7" :key="itemNum" :blockProps="blockProps" :itemNum="itemNum" :floorNum="floorNum" :blockNum="blockNum" :blockSide="blockSide"></BlockBodyItem>
  </div>
</template>

<script>
import BlockBodyItem from '@/components/BlockBodyItem.vue'
export default {
  name: 'BlockBodyFloor',
  props: ['blockProps', 'floorNum', 'blockSide', 'blockNum'],
  components: {
    BlockBodyItem
  }
}
</script>

