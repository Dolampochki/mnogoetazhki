<template>
  <div class="image-container" :style="`background-color: ${blockProps.imageBackground}`">
    <BlocksContainer :blockProps="blockProps"></BlocksContainer>
  </div>
</template>

<script>

import BlocksContainer from '@/components/BlocksContainer.vue'

export default {
  name: 'ImageContainer',
  props: ['blockProps'],
  components: {
    BlocksContainer
  }
}
</script>

