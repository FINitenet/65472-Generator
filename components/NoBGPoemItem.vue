<template>
  <h-stack class="mb-1">
    <div class="font-bold md:text-5xl text-4xl" v-bind:class="{'text-red-600': isRed, 'text-blue-800': !isRed}">
      <div v-if="itemString.length>0" class="md:m-1 m-0.5">
        {{ itemString }}
      </div>
      <div v-else class="md:m-1 m-0.5">&nbsp;</div>
    </div>
    <spacer/>
  </h-stack>
</template>

<script>
import HStack from "./utilities/layout/HStack";
import Spacer from "./utilities/layout/Spacer";
export default {
  name: "NoBGPoemItem",
  components: {Spacer, HStack},
  props: {
    itemString: String,
    isRed: Boolean
  }
}
</script>

<style scoped>

</style>
