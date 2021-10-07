<template>
  <div class="block-container" :style="`transform: scale(${blockProps.scale * 1});`">
    <Block v-for="blockNum in blockProps.blocksCount * 1" :blockProps="blockProps" :key="blockNum" :blockNum="blockNum"></Block>
  </div>
</template>

<script>
import Block from '@/components/Block.vue'
export default {
  name: 'BlocksContainer',
  props: ['blockProps'],
  components: {
    Block
  },
  data () {
    return {
    }
  },
  computed: {

  }
}
</script>

