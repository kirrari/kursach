<template>
  <div class="settings">
    <div class="settings__toggle">
      <span class="toggle__label">Тёмная тема: </span>
      <input
        type="checkbox"
        id="toggly"
      />
      <label
        for="toggly"
        class="toggle__toggly"
        ><i></i
      ></label>
    </div>
    <a class="settings__leave">Выйти из аккаунта</a>
  </div>
</template>

<script setup></script>

<style lang="scss" scoped>
.settings {
  display: flex;
  flex-direction: column;
  padding: 115px 60px;

  &__toggle {
    display: flex;
  }

  &__leave {
    color: #f00;
    font-size: 25px;
    margin-top: 15px;
    padding: 10px 0;
  }
}

.toggle {
  &__label {
    font-size: 25px;
    padding: 10px 0;
    margin-right: 40px;
  }

  &__toggly {
    align-self: center;
    cursor: pointer;
  }
}

label {
  display: block;
  width: 70px;
  height: 38px;
  border-radius: 100px;
  transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  background-color: #e6e9ec;
}

input {
  display: none;
}

i {
  height: 34px;
  width: 34px;
  background: #ffffff;
  display: inline-block;
  border-radius: 100px;
  margin-top: 2px;
  margin-left: 2px;
  transition: all 0.2s ease-in-out;
  -webkit-transition: all 0.2s ease-in-out;
  pointer-events: none;
  box-shadow: 0px 0px 0px 0px rgba(0, 0, 0, 0);
}

label:hover > i {
  box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.2);
  transform: scale(1.01);
}

input:checked + label > i {
  margin-left: 34px;
}

label:active {
  background-color: #a6b9cb;
}

label:active > i {
  width: 34px;
  box-shadow: 0px 2px 4px 0px rgba(0, 0, 0, 0.2);
}

input:checked + label:active > i {
  margin-left: 18px;
}

input:checked + label {
  background-color: #666;
}
</style>
