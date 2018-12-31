<template lang="html">
  <div class="CallToAction">
   <router-link v-if="type === 'internal' || content.type === 'internal'" :to="{ name: linkTo, params: btnParams }">
    {{ title || content.title }}
   </router-link>
   <a v-if="type === 'external' || content.type === 'external'" href="#">{{ title || content.title }}</a>
  </div>
</template>

<script>
export default {
 name: "CallToAction",
 props: {
  content: Object,
  linkTo: String,
  onClick: {
   type: Function
  },
  title: String,
  type: String
 }
}
</script>

<style lang="scss">
.CallToAction {}
</style>
