<template lang="html">
 <div id="progressBar">
  <div v-if="progressClass === 'active'" class="active">
   <div id="progression" :style="{ width: progressSize + '%' }"></div>
  </div>
 </div>
</template>

<script>
export default {
    name: "Progressbar",
    props: {
        progressClass: String,
        progressSize: Number
    }
}
</script>

<style lang="scss">

#progressBar {
    height: 10px;
    max-height: 10px;
    background-color: white;
    z-index: 2;
    .active {
        background-color: white;

        #progression {
            height: 10px;
            max-height: 10px;
            background-color: red;
            max-width: 100%;
            width: 0;
        }
    }
}
</style>
