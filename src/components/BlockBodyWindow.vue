<template>
  <div class="window">
    <div class="window-frame" :style="`background-color: ${blockProps.mainWindowBorderColor}`">
      <div class="window-glass" v-for="winItem in windowsCount" :key="winItem"
      :class="`${openedWindow(winItem) && 'opened'} ${halWindow && 'half'}`"
      :style="`border-color: ${side === 'center' ? blockProps.centerWindowBorderColor : blockProps.mainWindowBorderColor}`">
        <div v-if="halfWindow(winItem)" class="window-glass-half"
        :style="`border-color: ${side === 'center' ? blockProps.centerWindowBorderColor : blockProps.mainWindowBorderColor}`"></div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlockBodyWindow',
  props: ['blockProps', 'windowsCount', 'side', 'randomNum'],
  components: {

  },
  computed: {
    halWindow () {
      return this.randomNum > 0.5
    }
  },
  methods: {
    halfWindow (winItem) {
      if (winItem !== 1) return false
      if (this.side === 'center') return false
      return this.halWindow
    },
    openedWindow (winItem) {
      if (this.side === 'center') return false
      let modulus = this.blockProps.windowRandom
      let seed = (this.randomNum * 10 * winItem + winItem) % modulus
      let returnVal = seed / modulus
      return returnVal > 0.5
    }
  }
}
</script>

