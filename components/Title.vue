<template lang="html">
 <div class="Title">
  <h1 v-if="type === 'h1' || content.type === 'h1'" :class="className || content.className">{{ contentTitle || content.title }}</h1>
  <h2 v-if="type === 'h2' || content.type === 'h2'" :class="className || content.className">{{ contentTitle || content.title }}</h2>
  <h3 v-if="type === 'h3' || content.type === 'h3'" :class="className || content.className">{{ contentTitle || content.title }}</h3>
 </div>
</template>

<script>
export default {
 name: "Title",
 props: {
  content: Object,
  contentTitle: String,
  className: String,
  type: String
 }
}
</script>

<style lang="scss">
.Title {
}
</style>
