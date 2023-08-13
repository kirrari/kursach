<template>
  <div class="docs">
    <div class="data__field">
      <label
        for="passport-series"
        class="data__label"
        >Серия паспорта:</label
      >
      <input
        class="data__input"
        type="text"
        id="passport-series"
        placeholder="11 22"
      />
    </div>
    <div class="data__field">
      <label
        for="passport-number"
        class="data__label"
        >Номер паспорта:</label
      >
      <input
        class="data__input"
        type="text"
        id="passport-number"
        placeholder="123456"
      />
    </div>
    <div class="data__field">
      <label
        for="passport-code"
        class="data__label"
        >Код подразделения:</label
      >
      <input
        class="data__input"
        type="text"
        id="passport-code"
        placeholder="123-456"
      />
    </div>
    <div class="data__field">
      <label
        for="date-of-birth"
        class="data__label"
        >Дата рождения:</label
      >
      <input
        class="data__input"
        type="date"
        id="date-of-birth"
      />
    </div>
    <div class="data__field">
      <label
        for="date-of-passport"
        class="data__label"
        >Дата выдачи паспорта:</label
      >
      <input
        class="data__input"
        type="date"
        id="date-of-passport"
      />
    </div>
    <div class="data__field">
      <label
        for="place-of-birth"
        class="data__label"
        >Место рождения:</label
      >
      <input
        class="data__input"
        type="text"
        id="place-of-birth"
      />
    </div>
    <div class="data__field">
      <label
        for="issued-by-whom"
        class="data__label"
        >Кем выдан:</label
      >
      <textarea
        class="data__input"
        id="issued-by-whom"
      />
    </div>
    <div class="data__field">
      <label
        for="registration-address"
        class="data__label"
        >Адрес регистрации:</label
      >
      <input
        class="data__input"
        type="text"
        id="registration-address"
      />
    </div>
    <div class="data__field">
      <label
        for="passport-scans"
        class="data__label"
        >Сканы паспорта (основной разворот и прописка):</label
      >
      <input
        class="data__input"
        type="file"
        id="passport-scans"
        multiple
      />
    </div>
    <div class="data__field">
      <label
        for="snils-number"
        class="data__label"
        >Номер СНИЛС:</label
      >
      <input
        class="data__input"
        type="text"
        id="snils-number"
      />
    </div>
    <div class="data__field">
      <label
        for="snils-scan"
        class="data__label"
        >Скан СНИЛС:</label
      >
      <input
        class="data__input"
        type="file"
        id="snils-scan"
      />
    </div>
    <p class="data__diploma">Диплом об основном образовании</p>
    <div class="data__field">
      <label
        for="diploma-requisites"
        class="data__label"
        >Реквизиты диплома:</label
      >
      <input
        class="data__input"
        type="text"
        id="diploma-requisites"
      />
    </div>
    <div class="data__field">
      <label
        for="diploma-scan"
        class="data__label"
        >Скан диплома:</label
      >
      <input
        class="data__input"
        type="file"
        id="diploma-scan"
      />
    </div>
    <div class="data__field">
      <label
        for="additional-documents"
        class="data__label"
        >Дополнительные документы:</label
      >
      <input
        class="data__input"
        type="file"
        id="additional-documents"
        multiple
      />
    </div>
    <div class="data__btns">
      <button class="data__btn">Изменить данные</button>
      <button class="data__btn">Сохранить</button>
    </div>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.docs {
  display: flex;
  flex-direction: column;
  row-gap: 30px;
  margin: 30px 60px;
}
.data {
  &__field {
    display: grid;
    align-items: center;
    grid-template-columns: 400px 1fr;

    & > textarea {
      resize: none;
      height: 150px;
    }
  }

  &__label {
    font-size: 25px;
    margin-right: 30px;
  }

  &__input {
    width: 480px;
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

  &__diploma {
    font-size: 35px;
    margin: 30px 0 10px;
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
