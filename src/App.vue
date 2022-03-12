<template>
  <div class="content-wrapper h-100 overflow-auto" @scroll="handleScoll">
    <div
      class="content position-relative"
      :style="`background-image: url(${kvpenguins});`"
    >
      <navbar :is-top-sealed="isTopSealed" />
      <router-view />
    </div>
  </div>
</template>

<script>
  import Navbar from '@/components/Navbar/index.vue'
  import kvpenguins from '@/assets/kv-light.png'

  export default {
    components: { Navbar },
    data() {
      return {
        kvpenguins,
        isTopSealed: true,
      }
    },
    methods: {
      handleScoll() {
        this.isTopSealed =
          document.querySelector('.content-wrapper').scrollTop === 0
      },
    },
  }
</script>

<style lang="scss">
  @import url('https://cdnjs.cloudflare.com/ajax/libs/bootstrap/5.1.3/css/bootstrap.min.css');

  #app {
    font-family: Avenir, Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;

    height: 100vh;
  }

  a {
    text-decoration: none;
  }

  .fs-3.fw-bold {
    border-bottom: 3px solid lightblue;
  }

  .content-center {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  /* .container {
    padding-top: 3rem !important;
  } */

  .content {
    background-image: none !important;
    background-repeat: no-repeat;
    background-position: center center;
    background-attachment: scroll;
    background-size: cover;
  }
</style>
