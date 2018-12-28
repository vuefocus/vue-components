<template lang="html">
 <div class="Button">
  <router-link v-if="type === 'link'" :to="{ name: link, params: {} }">
   <button :class="className">
    {{ title }}
   </button>
  </router-link>
  <button v-if="type === 'disabled'" :class="type">
   {{ title }}
  </button>
  <button v-if="type === 'onClick'" :class="className" @click="onClick">
   {{ title }}
  </button>
 </div>
</template>

<script>
export default {
    name: "Button",
    props: {
     className: String,
     content: Object,
     title: String,
     link: String,
     onClick: {
      type: Function
     },
     type: String
    }
}
</script>

<style lang="scss">
.Button {}
</style>
