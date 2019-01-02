<template lang="html">
 <div class="Button">
  <router-link v-if="type === 'link' || content.type === 'link'" :to="{ name: link || content.link, params: {} }">
   <button :class="className || content.className">
    {{ title || content.title }}
   </button>
  </router-link>
  <button v-if="type === 'external' || content.type === 'external'" :class="className || content.type" @click="goToPage(content.link)">
    {{ title || content.title }}
  </button>
  <button v-if="type === 'disabled' || content.type === 'disabled'" :class="type || content.type">
    {{ title || content.title }}
  </button>
  <button v-if="type === 'onClick' || content.type === 'onClick'" :class="className || content.type" @click="onClick">
    {{ title || content.title }}
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
 },
 methods: {
  goToPage(link) {
   window.open(link)
  }
 }
}
</script>

<style lang="scss">
.Button {
    button {
        &:focus {
            outline: none;
            box-shadow: none;
        }
    }
    .disabled {
        opacity: 0.25;
    }
}
</style>
