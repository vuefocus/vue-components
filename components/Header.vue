<template lang="html">
  <header :class="className">
   {{ title }}
  </header>
</template>

<script>
export default {
 name: "Header",
 props: {
  className: String,
  onClick: {
   type: Function
  },
  title: String
 }
}
</script>

<style lang="scss">
header {}
</style>
