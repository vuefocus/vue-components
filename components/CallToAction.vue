<template lang="html">
  <div class="CallToAction">
   <router-link v-if="type === 'internal' || content.type === 'internal'" :to="{ name: link || content.link, params: btnParams }">
    {{ title || content.title }}
   </router-link>
   <a v-if="type === 'external' || content.type === 'external'" :href="link || content.link" target="_blank">{{ title || content.title }}</a>
  </div>
</template>

<script>
export default {
 name: "CallToAction",
 props: {
  content: Object,
  link: String,
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
