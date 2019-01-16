<template lang="html">
  <div class="Input">
   <label v-if="content.label">{{ content.label }}</label>
   <input :class="className || content.className" :placeholder="inputPlaceholder || content.inputPlaceholder">
  </div>
</template>

<script>
export default {
 name: "Input",
 data() {
  return {
   attachment: undefined
  }
 },
 props: {
  className: String,
  content: Object,
  inputPlaceholder: String,
  onClick: {
   type: Function
  },
  title: String
 }
}
</script>

<style lang="scss">
.Input {
    input {
        &:focus {
            outline: none;
            box-shadow: none;
            transition: 0.25s;
        }

    }
}
</style>
