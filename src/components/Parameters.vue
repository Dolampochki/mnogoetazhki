<template>
  <div class="parameters">
    <ul>
      <li>
        <input v-model="blockParameters.scale" type="range" min="0.3" max="3" step="0.1">
      </li>
      <li>
        <input v-model="blockParameters.blocksCount" type="range" min="1" max="5">
      </li>
      <li>
        <input v-model="blockParameters.floorsCount" type="range" min="5" max="16">
      </li>
      <li>
        <input v-model="blockParameters.windowRandom" type="range" min="3" max="16" step="1">
      </li>
      <li>
        <input v-model="blockParameters.imageBackground" type="color">
      </li>
      <li>
        <input v-model="blockParameters.mainBlockItemColor" type="color">
      </li>
      <li>
        <input v-model="blockParameters.centerBlockItemColor" type="color">
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Parameters',
  props: ['blockProps'],
  data () {
    return {
      blockParameters: this.blockProps
    }
  }
}
</script>

