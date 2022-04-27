<template>
  <div
    class="bg-gray-400"
    :class="[{'horizontal-divider-size mx-2 my-0.5': horizontal},{'vertical-divider-size my-2 mx-0.5': !horizontal}]"
  />
</template>

<script>
export default {
  name: "Divider",
  props: {
    horizontal: {
      type: Boolean,
      default: true
    }
  }
}
</script>

<style scoped>

</style>
