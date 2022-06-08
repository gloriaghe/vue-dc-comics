<template>
  <div id="app">
    <HeaderDC/>
    <main>
        <SectionDC/>
        <SectionLink/>
    </main>
    <FooterDC/>
  </div>
</template>

<script>
import HeaderDC from './components/HeaderDC.vue'
import SectionDC from './components/SectionDC.vue'
import SectionLink from './components/SectionLink.vue'
import FooterDC from './components/FooterDC.vue'

export default {
  name: 'App',
  components: {
    HeaderDC,
    SectionDC,
    SectionLink,
    FooterDC
  }
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  @mixin my-flex{
        display: flex;
        flex-direction: row;
    };
}
</style>
