<template lang="html">
  <div class="Card">
   {{ content }}
  </div>
</template>

<script>
export default {
 name: "Card",
 props: {
  content: Object,
  onClick: {
   type: Function
  }
 }
}
</script>

<style lang="scss">
.Card {
    padding: 25px;
    margin: 0 0 20px;
    -webkit-box-shadow: 0 0 35px 5px rgba(0, 0, 0, 0.045);
    -moz-box-shadow: 0 0 35px 5px rgba(0, 0, 0, 0.045);
    box-shadow: 0 0 35px 5px rgba(0, 0, 0, 0.045);
}
</style>
