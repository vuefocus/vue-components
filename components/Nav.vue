<template lang="html">
  <nav :class="className">
   <ul v-if="content">
    <li v-for="el in content">
     <router-link :to="{ name: el.link, params: {} }">
      {{ el.title }}
     </router-link>
    </li>
   </ul>
  </nav>
</template>

<script>
export default {
 name: "Navigation",
 props: {
  className: String,
  content: Object
 }
}
</script>

<style lang="scss">
nav {}
</style>
