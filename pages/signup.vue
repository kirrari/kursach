<template>
  <form class="signup">
    <h2 class="signup__title">Регистрация</h2>
    <input
      type="text"
      placeholder="Логин"
    />
    <input
      type="email"
      placeholder="Почта"
    />
    <input
      type="password"
      placeholder="Пароль"
    />
    <button class="signup__btn">Зарегестрироваться</button>
    <NuxtLink
      to="/login"
      class="signup__link"
      >Вернуться ко входу</NuxtLink
    >
  </form>
</template>

<script setup></script>

<style lang="scss" scoped>
.signup {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin: 175px auto 0;
  gap: 20px;

  &__title {
    font-family: Inter;
    font-size: 70px;
    font-style: normal;
    font-weight: 400;
    line-height: normal;
  }

  & > input {
    position: relative;
    width: 387px;
    height: 60px;
    font-size: 28px;
    padding: 10px 30px;
    border-radius: 16px;
    background: #dadada;
    box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.05),
      0px -3px 8px 0px rgba(0, 0, 0, 0.03);
    border: none;

    &::placeholder {
      position: absolute;
      top: 13px;
      color: #969696;
      font-size: 28px;
    }
  }

  &__btn {
    width: 337px;
    height: 60px;
    padding: 10px 30px;
    border-radius: 16px;
    background: #0f244d;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    color: #fff;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    font-size: 24px;
    cursor: pointer;
  }

  &__link {
    color: #2877b4;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    font-size: 20px;
  }
}
</style>
