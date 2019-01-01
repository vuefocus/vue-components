<template lang="html">
 <div class="Message" :class="className || content.className">
  <p v-for="el, index in content.paragraph" :key="index">{{ el }}</p>
 </div>
</template>

<script>
export default {
 name: "Message",
 props: {
  content: Object,
  className: String,
  title: String,
  type: String
 }
}
</script>

<style lang="scss">
.Message {
    max-width: 300px;
    position: absolute;
    bottom: 25px;
    right: 25px;
    color: white;
    padding: 15px;
    border-radius: 5px;
    opacity: 0;
    animation-name: slidein;
    animation-duration: 6s;
}

@keyframes slidein {
    0% {
        opacity: 0;
    }

    15% {
        opacity: 1;
    }

    85% {
        opacity: 1;
    }

    100% {
        opacity: 0;
    }
</style>
