<template>
  <div class="container">
    <div class="image">
      <ImageContainer :blockProps="blockProps"></ImageContainer>
    </div>
    <Parameters :blockProps="blockProps"></Parameters>
  </div>
</template>

<script>
import ImageContainer from '@/components/ImageContainer.vue'
import Parameters from '@/components/Parameters.vue'

export default {
  name: 'App',
  components: {
    ImageContainer,
    Parameters
  },
  data () {
    return {
      blockProps: {
        blocksCount: 2,
        floorsCount: 9,
        scale: 1,
        windowRandom: 5,
        imageBackground: '#E2E0BA',
        mainBlockItemColor:'#b2bcc4',
        centerBlockItemColor: '#ab464f',
        brickColor: '#804046',
        doorColor: '#575f62',
        enteranceColor: '#6c2930',
        enteranceHeadColor: '#8f9ea9',
        mainBlockBorderColor: '#dce3ed',
        centerBlockBorderColor: '#ab464f',
        mainBlockInnerBorderColor: '#804046',
        centerBlockInnerBorderColor: '#6c2930',
        mainWindowBorderColor: '#dae1e9',
        centerWindowBorderColor: '#44494c',
        centerWindowColor: '#767d83',
        stairsColor: '#767d83',
        blockBorderColor: '#459250',
        blockInnerBorderColor: '#8f9ea9',
        handrailColor: '#6799bb',
        headColor: '#8f9ea9',
      }
    }
  }
}
</script>

