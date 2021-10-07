<template>
  <div class="block-body-item" :class="`item-${itemNum} ${side} ${floorNum === blockProps.floorsCount * 1 && 'last'}`"
  :style="`border-color: ${side === 'center' ? blockProps.centerBlockInnerBorderColor : blockProps.mainBlockInnerBorderColor};
  background-color: ${side === 'center' ? blockProps.centerBlockBorderColor : blockProps.mainBlockBorderColor};`">

    <BlockHeadLoft v-if="floorNum === blockProps.floorsCount * 1 && side === 'center'" :blockProps="blockProps"></BlockHeadLoft>
    <div class="block-body-item-inner" :style="`background-color: ${side === 'center' ? blockProps.centerBlockItemColor : blockProps.mainBlockItemColor};`">
      <BlockEnterance v-if="floorNum === 1 && side === 'center'" :blockProps="blockProps"></BlockEnterance>
      <BlockBodyWindow v-else :blockProps="blockProps" :windowsCount="windowsCount" :side="side" :randomNum="randomNum"></BlockBodyWindow>

    </div>
  </div>
</template>

<script>
import BlockBodyWindow from '@/components/BlockBodyWindow.vue'
import BlockEnterance from '@/components/BlockEnterance.vue'
import BlockHeadLoft from '@/components/BlockHeadLoft.vue'
export default {
  name: 'BlockBodyItem',
  props: ['blockProps', 'itemNum', 'floorNum', 'blockSide', 'blockNum'],
  components: {
    BlockBodyWindow,
    BlockEnterance,
    BlockHeadLoft
  },
  computed: {
    side () {
      return this.itemNum === 4 ? 'center' : this.itemNum < 4 ? 'left' : 'right'
    },
    windowsCount () {
      let winCount = 2
      if (this.itemNum === 2 || this.itemNum === 6) winCount = 3
      if (this.blockSide.includes('left') && this.itemNum === 1) winCount = 3
      if (this.blockSide.includes('right') && this.itemNum === 7) winCount = 3
      if (this.itemNum === 4) winCount = 3
      return winCount
    },
    randomNum () {
      let modulus = this.blockProps.windowRandom
      let seed = this.itemNum
      seed = (this.floorNum * seed + this.blockNum) % modulus
      let returnVal = seed / modulus
      return returnVal
    }
  }
}
</script>

