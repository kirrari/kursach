<template>
  <header class="header">
    <div class="header__container">
      <img
        src="/assets/logo.svg"
        alt="ЦНИИ русского жестового языка"
        class="header__logo"
      />
      <h2 class="header__text">
        Аттестация переводчиков русского жестового языка
      </h2>
      <NuxtLink
        to="/"
        class="header__profile"
        v-if="!isLoginPage"
        >Профиль</NuxtLink
      >
    </div>
  </header>
</template>

<script setup>
const isLoginPage = useRoute().name === 'login' || useRoute().name === 'signup';
</script>

<style lang="scss" scoped>
.header {
  &__container {
    display: flex;
    align-items: center;
    padding: 20px 50px;
    border-bottom: 2px solid #dadada;
  }

  &__logo {
    width: 116px;
    height: 116px;
  }

  &__text {
    font-size: 30px;
    font-weight: 400;
    max-width: 500px;
    margin-left: 50px;
    margin-right: auto;
  }

  &__profile {
    font-size: 30px;
  }
}
</style>
