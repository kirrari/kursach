<template>
  <div id="app">
    <Header />
    <div :class="{ content: !isLoginPage }">
      <Sidebar
        class="content__sidebar"
        v-if="!isLoginPage"
      />
      <RouterView class="content__main" />
    </div>
  </div>
</template>

<script setup>
const isLoginPage = useRoute().name === 'login' || useRoute().name === 'signup';
</script>

<style lang="scss">
#app {
  height: 100%;
}

.content {
  height: 75%;
  display: grid;
  grid-template-columns: 240px 1fr;
  margin: 0 150px;

  &__sidebar {
    padding-top: 115px;
    border-right: 2px solid #dadada;
    filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
  }

  &__main {
    width: 100%;
    margin: 0 auto;
  }
}
</style>
