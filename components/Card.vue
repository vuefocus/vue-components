<template lang="html">
  <div class="Card">
   <p v-if="content" v-for="el, index in content" :key="index">{{ el }}</p>
   <p v-if="array" v-for="el, index in array" :key="index">{{ el }}</p>
  </div>
</template>

<script>
export default {
 name: "Card",
 props: {
  content: Object,
  array: Array,
  onClick: {
   type: Function
  }
 }
}
</script>

<style lang="scss">
.Card {
}
</style>
