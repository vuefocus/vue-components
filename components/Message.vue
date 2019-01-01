<template lang="html">
 <div class="Message">
  <p v-for="el, index in content.paragraph" :key="index">{{ el }}</p>
 </div>
</template>

<script>
export default {
 name: "Message",
 props: {
  content: Object,
  className: String,
  title: String,
  type: String
 }
}
</script>

<style lang="scss">
.Message {}
</style>
