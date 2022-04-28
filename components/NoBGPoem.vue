<template>
  <v-stack>
    <NoBGPoemItem :is-red="true" :item-string="poem.first" />
    <NoBGPoemItem :is-red="false" :item-string="poem.second" />
    <NoBGPoemItem :is-red="true" :item-string="poem.third" />
    <NoBGPoemItem :is-red="false" :item-string="poem.fourth" />
    <NoBGPoemItem :is-red="true" :item-string="poem.fifth" />
    <h-stack v-if="poem.author.length>0" class="mb-1">
      <div class="font-bold text-md text-gray-700">
        <div class="md:m-1 m-0.5">
          @{{ poem.author }}
        </div>
      </div>
      <spacer/>
    </h-stack>
  </v-stack>
</template>

<script>
import HStack from "./utilities/layout/HStack";
import VStack from "./utilities/layout/VStack";
import Spacer from "./utilities/layout/Spacer";
import NoBGPoemItem from "./NoBGPoemItem";
export default {
  name: "NoBGPoem",
  components: {NoBGPoemItem, Spacer, VStack, HStack},
  props:{
    poem: {
      first: String,
      second: String,
      third: String,
      fourth: String,
      fifth: String,
      author: String
    }
  }
}
</script>

<style scoped>

</style>
