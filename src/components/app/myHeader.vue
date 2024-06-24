<script setup>
// import router from '@/router';
const links = [
  { title: "Курсы", route: "/" },
  { title: "Коворкинг", route: "/" },
  { title: "Контакты", route: "/" },
  { title: "Локация", route: "/" },
]

</script>

<template>
  <header class="header">
    <div class="header__nav">
      <div class="header__nav-nav container">
        <div class="header__nav-logo">
          <img src="@/assets/img/WEBSTEP (4) 1.png" alt="WEBSTEP" />
        </div>
        <div class="header__nav-title">
          <ul class="header__nav-list">
            <li class="header__nav-item" v-for="link of links" :key="link.title">
              <router-link :to="link.route" class="header__nav-link">{{ link.title }}</router-link>
            </li>
          </ul>
        </div>
        <div class="header__nav-logo">
          <img src="@/assets/img/Дизайн без названия (29) 1.png" alt="" />
        </div>
      </div>
    </div>
    <div class="header__info container-fluid">
      <div class="header__info-info container">
        <div class="header__info-p">
          <p class="header__info-title">Курсы Современных Профессий</p>
          <div class="header__info-button">
            <button class="header__info-btn">Начать обучение</button>
          </div>
        </div>
        <div class="header__info-image">
          <img
            src="@/assets/img/WEBSTEP (6) 1.png"
            alt=""
            class="header__info-img"
          />
        </div>
      </div>
    </div>
  </header>
</template>

<style lang="scss" scoped>
.header {
  background: linear-gradient(270deg, #415a77 -32.97%, #1b263b 92.7%);

  &__nav {
    padding: 65px 0;
  }

  &__nav-nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__nav-list {
    display: flex;
    gap: 49px;
  }

  &__nav-link {
    color: #fff;
    font-weight: 400;
    line-height: 75px;
  }

  &__info {
    background: linear-gradient(270deg, #415a77 -32.97%, #111b2c 92.7%);
    border-radius: 20px 20px 0 0;
    box-shadow: 0px 4px 50px 0px #00000040;
  }

  &__info-info  {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  &__info-title {
    width: 617px;
    font-weight: 700;
    font-size: 65px;
    line-height: 75px;
    color: #fff;
    padding-bottom: 50px;
  }

  &__info-btn {
    width: 428px;
    font-size: 40px;
    padding: 15px 29px;
    border-radius: 15px;
    border-inline: none;
    color: #415A77 ;
    cursor: pointer;
  }
}
</style>

