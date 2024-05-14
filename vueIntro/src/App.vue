<script setup>
  import HelloWorld from './components/HelloWorld.vue'

  import Directives from './components/TheDirectives.vue'
  import CompositionApi from './components/Composition.vue'
  import DescComputed from './components/Computed.vue'
  import Bindings from './components/ClassStyleBinding.vue'
  import Conditional from './components/ConditionalRendering.vue'
  import ListRender from './components/ListRendering.vue'
  import FormInputs from './components/FormInputBinding.vue'
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="./assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <HelloWorld msg="Table of Contents" />
    </div>
  </header>

  <main>
    <!--- <TheWelcome /> -->
    <Directives />
    <CompositionApi />
    <DescComputed />
    <Bindings />
    <Conditional/>
    <ListRender/>
    <FormInputs/>
  </main>
</template>

<style scoped>
  header {
    line-height: 1.5;
  }

  .logo {
    display: block;
    margin: 0 auto 2rem;
  }

  @media (min-width: 1024px) {
    header {
      display: flex;
      place-items: center;
      padding-right: calc(var(--section-gap) / 2);
    }

    .logo {
      margin: 0 2rem 0 0;
    }

    header .wrapper {
      display: flex;
      place-items: flex-start;
      flex-wrap: wrap;
    }
  }
</style>
