<template>
  <div class="enterance" :style="`background-color: ${blockProps.enteranceColor}`">
    <div class="enterance-head" :style="`background-color: ${blockProps.enteranceHeadColor}`"></div>
    <div class="enterance-body">
      <div class="enterance-door left" :style="`background-color: ${blockProps.doorColor}`"></div>
      <div class="enterance-door right" :style="`background-color: ${blockProps.doorColor}`"></div>
    </div>
    <div class="enterance-footer">
      <ul class="enterance-stairs" :style="`background-color: ${blockProps.stairsColor}`">
        <li class="stair" v-for="stair in 4" :key="stair"></li>
      </ul>
      <div class="handrail" :style="`background-color: ${blockProps.handrailColor}`"></div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'BlockEnterance',
  props: ['blockProps'],
  components: {

  }
}
</script>

