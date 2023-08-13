<template>
  <div class="profile">
    <div class="profile__data">
      <div class="data__field">
        <label
          for="lastname"
          class="data__label"
          >Фамилия:</label
        >
        <input
          class="data__input"
          type="text"
          id="lastname"
        />
      </div>
      <div class="data__field">
        <label
          for="firstname"
          class="data__label"
          >Имя:</label
        >
        <input
          class="data__input"
          type="text"
          id="firstname"
        />
      </div>
      <div class="data__field">
        <label
          for="middlename"
          class="data__label"
          >Отчество:</label
        >
        <input
          class="data__input"
          type="text"
          id="middlename"
        />
      </div>
      <div class="data__fieldset">
        <span>Пол:</span>
        <div>
          <input
            class="data__radio"
            type="radio"
            id="male"
            name="gender"
            checked
          />
          <label
            for="male"
            class="data__label"
            >Мужской</label
          >
          <input
            class="data__radio"
            type="radio"
            id="female"
            name="gender"
          />
          <label
            for="female"
            class="data__label"
            >Женский</label
          >
        </div>
      </div>
      <div class="data__field">
        <label
          for="mobile-phone"
          class="data__label"
          >Мобильный телефон:</label
        >
        <input
          class="data__input"
          type="tel"
          id="mobile-phone"
          placeholder="+7 (999) 123-45-67"
        />
      </div>
      <div class="data__field">
        <label
          for="office-phone"
          class="data__label"
          >Рабочий телефон:</label
        >
        <input
          class="data__input"
          type="tel"
          id="office-phone"
          placeholder="+7 (999) 123-45-67"
        />
      </div>
      <div class="data__field">
        <label
          for="email"
          class="data__label"
          >Электронная почта:</label
        >
        <input
          class="data__input"
          type="email"
          id="email"
        />
      </div>
      <div class="data__field">
        <label
          for="mail"
          class="data__label"
          >Почтовый адрес:</label
        >
        <input
          class="data__input"
          type="text"
          id="mail"
        />
      </div>
      <div class="data__btns">
        <button class="data__btn">Изменить данные</button>
        <button class="data__btn">Сохранить</button>
      </div>
    </div>
    <img
      class="profile__img"
      src="@/assets/profile-logo.png"
    />
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.profile {
  margin: 30px 60px;
  display: flex;

  &__data {
    max-width: 722px;
    margin-right: 100px;
    display: flex;
    flex-direction: column;
    row-gap: 30px;
    flex: 1 1 100%;
  }

  &__img {
    max-width: 300px;
    max-height: 400px;
  }
}
.data {
  &__field {
    display: grid;
    align-items: center;
    grid-template-columns: 300px 1fr;
  }

  &__label {
    font-size: 25px;
    margin-right: 30px;
  }

  &__input {
    width: 420px;
    height: 60px;
    flex: 0 1 420px;
    font-size: 25px;
    padding: 10px 30px;
    border: none;
    border-radius: 16px;
    background: #dadada;
    box-shadow: 0px 3px 8px 0px rgba(0, 0, 0, 0.05),
      0px -3px 8px 0px rgba(0, 0, 0, 0.03);

    &:focus {
      outline-color: rgb(50, 115, 246);
    }
  }

  &__fieldset {
    display: flex;
    font-size: 25px;

    & > span {
      width: 270px;
      margin-right: 30px;
    }

    & > div {
      width: 420px;
      display: flex;
      align-items: center;
    }
  }

  &__radio {
    width: 24px;
    height: 24px;
    margin-right: 10px;
    cursor: pointer;
  }

  &__btns {
    margin-top: 40px;
    display: flex;
    column-gap: 30px;
  }

  &__btn {
    color: #fff;
    font-size: 20px;
    padding: 10px 30px;
    border-radius: 20px;
    background: #0f244d;
    box-shadow: 0px 4px 4px 0px rgba(0, 0, 0, 0.25);
    cursor: pointer;
  }
}
</style>
