<template lang="html">
  <input v-model="attachment" :class="className" :placeholder="inputPlaceholder" @input="showMe">
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
  inputPlaceholder: String,
  onClick: {
   type: Function
  },
  title: String
 },
 methods: {
  showMe() {
   console.log(this.attachment)
  }
 }
}
</script>

<style lang="scss">
input {
    }
</style>
