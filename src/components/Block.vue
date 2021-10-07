<template>
  <div class="block" :class="blockSide">
    <BlockHead :blockProps="blockProps"></BlockHead>
    <BlockBody :blockProps="blockProps" :blockNum="blockNum" :blockSide="blockSide"></BlockBody>
    <BlockFooter :blockProps="blockProps"></BlockFooter>
  </div>
</template>

<script>
import BlockHead from '@/components/BlockHead.vue'
import BlockBody from '@/components/BlockBody.vue'
import BlockFooter from '@/components/BlockFooter.vue'
export default {
  name: 'BlocksContainer',
  props: ['blockProps', 'blockNum'],
  components: {
    BlockHead,
    BlockBody,
    BlockFooter
  },
  computed: {
    blockSide () {
      let blockSideClass = ''
      if (this.blockNum === 1) blockSideClass += 'left '
      if (this.blockNum === this.blockProps.blocksCount * 1) blockSideClass += 'right '
      return blockSideClass
    }
  }
}
</script>

