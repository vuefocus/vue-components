<template lang="html">
 <div class="Accordion">
  <div class="option" v-for="(question, index) in content" :key="index">
   <header @click="reveal(index)">{{ question.title }}</header>
   <p v-if="selected === index" class="text">{{ question.description }}</p>
  </div>
 </div>
</template>

<script>
export default {
 name: "Accordion",
 data() {
  return {
   selected: false
  }
 },
 props: {
  content: Object
 },
 methods: {
  reveal(index) {
   this.selected = index
  }
 }
}
</script>

<style scoped lang="scss">
.Accordion {
    padding: 15px 0;

    .arrowInvert {
        width: 15px;
        filter: invert(100%);
        transform: rotate(90deg);
        transition: 0.25s;
    }

    .arrowTop {
        transform: rotate(270deg);
    }

    .option {
        padding: 15px 0;
        header {
            border-bottom: 1px solid grey;
            padding-bottom: 15px;
            margin-bottom: 15px;
            p {
                font-family: Gotham;
                font-size: 20px;
                font-weight: bold;
                font-style: normal;
                font-stretch: normal;
                line-height: normal;
                letter-spacing: normal;
                color: grey;
                margin-bottom: 0;
            }
        }
    }
}
</style>
