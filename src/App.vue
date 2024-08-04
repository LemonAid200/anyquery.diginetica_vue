<template>
  <div id="app">
      <VueHeader/>
      <div class="main">
        <VueFilters/>
        <VueProductsList/>
      </div>
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'
import VueHeader from './components/VueHeader.vue'
import VueFilters from './components/VueFilters.vue'
import VueProductsList from './components/VueProductsList.vue'

export default {
  name: 'App',
  components: {
    VueHeader,
    VueFilters,
    VueProductsList
  }
}
</script>

<style lang="scss">
@import "./styles/variables";


#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;

  width: 100%;
  max-width: 1720px;
  margin: 0 100px;
}


@media (max-width: $layout-breakpoint-extra-large) {
  #app {
    margin: 0 16px;

  }
}

body {
  @include unset-default();
  @include custom-scroll();
  display: flex;
  justify-content: center;
  padding-bottom: 50px;
  overflow-y: auto;
  overflow-x: clip;

  h3 {
    font-size: 16px;
    line-height: 19px;
    letter-spacing: 0%;
    text-align: center;
    font-weight: 400;
  }
  button {
    cursor: pointer;
  }
  ul{
      @include unset-default();
  }
  .main {
    margin-top: 36px;
    display: grid;
    gap: 36px;
    grid-template-columns: 280px 1fr;

    font-family: PT Sans;
    font-size: 14px;
    font-weight: 400;
    line-height: 16px;
  }

  @media (max-width: $layout-breakpoint-small) {
  .main {
    grid-template-columns: 1fr;
    margin: 0 16px;
  }
}

}


</style>
