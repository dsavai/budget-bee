<template>
  <section class="main-conatiner">
    <Header />
    <main id="main">
      <router-view />
    </main>
    <BottomFixedMenu />
  </section>
  
</template>

<script>
import Header from "@/components/header/Header.vue"
import BottomFixedMenu from "@/components/navigation/BottomFixedMenu.vue"

export default {
  name: "App",
  components: {
    Header,
    BottomFixedMenu
  }
}
</script>

<style lang="scss">
  *,
  *::before,
  *::after{
    box-sizing: border-box;
    margin: 0;
    padding: 0;
  }
  body{
    font-family: 'Montserrat Alternates', sans-serif;
    background: #f2f2f2;
    color: #151515;
    overflow-x: hidden;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
  }
  body,
  div,
  p{
    font-size: 14px;
  }

  .main-conatiner{
    background: #fff;
    width: 480px;
    margin: 0 auto;
  }
</style>
