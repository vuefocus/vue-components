<template lang="html">
  <div class="Ticket">
   {{ array }}
  </div>
</template>

<script>
export default {
 name: "Ticket",
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
.Ticket {
}
</style>
