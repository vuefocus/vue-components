<template lang="html">
  <div class="Sit">
  </div>
</template>

<script>
export default {
 name: "Sit",
 data() {
  return {}
 },
 props: {
  onClick: {
   type: Function
  },
  content: Object,
  orientation: Number
 },
 methods: {}
}
</script>

<style lang="scss">
@import "../assets/scss/colors.scss";

.Sit {
    background: white;
    border: 3px solid $lightgrey;
    width: 25px;
    height: 25px;
    border-top-left-radius: 80px;
    border-top-right-radius: 80px;

    .full {
        background: $lightgrey;
    }

    .selected {
        border: 3px solid $summer;
        background: $summer;
    }
}
</style>
