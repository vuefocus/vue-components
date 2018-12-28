<template lang="html">
  <div class="CallToAction">
   <router-link v-if="linkTo" :to="{ name: linkTo, params: btnParams }">
    {{ title }}
   </router-link>
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
  title: String
 }
}
</script>

<style lang="scss">
.CallToAction {
    }
</style>
