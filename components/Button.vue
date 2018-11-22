<template lang="html">
 <div class="Button">
  <router-link v-if="type === 'link'" :to="{ name: link, params: {} }">
   <button :class="className">
    {{ contentButton }}
   </button>
  </router-link>
  <button v-if="type === 'disabled'" :class="type">
   {{ contentButton }}
  </button>
  <button v-if="type === 'onClick'" :class="className" @click="onClick">
   {{ contentButton }}
  </button>
 </div>
</template>

<script>
export default {
    name: "Button",
    props: {
     className: String,
     contentButton: String,
     link: String,
     onClick: {
      type: Function
     }
     type: String
    }
}
</script>

<style lang="scss">
.Button {}
</style>
