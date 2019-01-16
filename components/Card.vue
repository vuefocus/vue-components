<template lang="html">
  <div class="Card">
   <img v-if="imgSrc || content.image" :src="imgSrc || content.image" :alt="imgSrc || content.image">
   <p v-if="content" v-for="el, index in content" :key="index">{{ el }}</p>
   <p v-if="array" v-for="el, index in array" :key="index">{{ el }}</p>
  </div>
</template>

<script>
export default {
 name: "Card",
 props: {
  array: Array,
  content: Object,
  imgSrc: String,
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
