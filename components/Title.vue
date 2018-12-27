<template lang="html">
 <div class="title">
  <h1 v-if="type === 'h1'" :class="className">{{ contentTitle }}</h1>
  <h2 v-if="type === 'h2'" :class="className">{{ contentTitle }}</h2>
  <h3 v-if="type === 'h3'" :class="className">{{ contentTitle }}</h3>
  <p v-if="subtitle">{{ contentSubtitle }}</p>
 </div>
</template>

<script>
export default {
    name: "title",
    props: {
     contentTitle: String,
     contentSubtitle: String,
     className: String,
     subtitle: String,
     type: String
    }
}
</script>

<style lang="scss">
#title {}
</style>
