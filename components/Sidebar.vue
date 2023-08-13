<template>
  <aside class="sidebar">
    <NuxtLink
      to="/"
      class="sidebar__link"
      exactActiveClass="active-link"
      >Личные данные</NuxtLink
    >
    <NuxtLink
      to="/docs"
      class="sidebar__link"
      exactActiveClass="active-link"
      >Документы</NuxtLink
    >
    <NuxtLink
      to="/settings"
      class="sidebar__link"
      exactActiveClass="active-link"
      >Настройки</NuxtLink
    >
  </aside>
</template>

<script setup></script>

<style lang="scss" scoped>
.sidebar {
  display: flex;
  flex-direction: column;
  row-gap: 15px;

  &__link {
    font-size: 25px;
    padding: 10px 20px;
  }
}

.active-link {
  border: 2px solid #dadada;
  border-right: none;
  border-radius: 10px 0 0 10px;
}
</style>
