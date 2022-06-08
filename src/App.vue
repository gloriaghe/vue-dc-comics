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
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  text-align: center;
  color: black;
  display: flex;
  flex-direction: column;
  justify-content: space-between;

}
</style>
