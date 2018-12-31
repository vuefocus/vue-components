<template lang="html">
  <div class="Description">
   <p>{{ title || content.title }}</p>
  </div>
</template>

<script>
export default {
 name: "Description",
 props: {
  content: Object,
  onClick: {
   type: Function
  },
  title: String
 }
}
</script>

<style lang="scss">
.Description {}
</style>
