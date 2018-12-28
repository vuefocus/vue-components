<template lang="html">
  <div class="loader">
   <p>Loader</p>
  </div>
</template>

<script>
export default {
 name: "loader",
}
</script>

<style scoped lang="scss">
@import "../assets/styles/colors.scss";

.loader {
    text-align: center;
    margin: 15px 0;
    width: 100%;

    img {
        animation-name: spin;
        animation-duration: 1000ms;
        animation-iteration-count: infinite;
        animation-timing-function: linear;
    }
}

@-moz-keyframes spin {
    from {
        -moz-transform: rotate(0deg);
    }
    to {
        -moz-transform: rotate(360deg);
    }
}
@-webkit-keyframes spin {
    from {
        -webkit-transform: rotate(0deg);
    }
    to {
        -webkit-transform: rotate(360deg);
    }
}
@keyframes spin {
    from {
        transform: rotate(0deg);
    }
    to {
        transform: rotate(360deg);
    }
}
</style>
