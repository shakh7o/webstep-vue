<script setup>
const links = [
  { title: "Веб Программирование", route: "/web", images: "img-1",},
  { title: "Дропшиппинг", route: "/", images: "img-2",},
  { title: "Интернет Маркетинг", route: "/", images: "img-3",},
  { title: "Scratch", route: "/", images: "img-4",},
  { title: "Full Дизайн", route: "/", images: "img-5"},
  { title: "3Ds Max", route: "/", images: "img-6"},
];
const image = [
  { img: "web4", text: "В ГРУППЕ" },
  { img: "web2", text: "ИНДИВИДУАЛЬНО" },
  { img: "web3", text: "ОЧНО" },
  { img: "web4", text: "ОНЛАЙН" }
]
</script>

<template>
  <div class="main">
    <div class="main__info-content">
      <div class="main__content" v-for="(img, idx) of links" :key="idx">
        <img
          :src="`/src/assets/img/${img.images}.png`"
          alt=""
          class="main__content-image"
        />
        <div class="main__content-text">
        <router-link :to="img.route" class="main__content-text">{{ img.title }}</router-link>
      </div>
      </div>
    </div>
    <div class="main__info">
      <div class="main__info-info container-fluid">
        <h2 class="main__info-title">Почему мы?</h2>
        <p class="main__info-text">Наша миссия - вдохновить и поддержать вас в достижении ваших целей в области технологий. Мы предлагаем широкий спектр курсов и тренингов, разработанных экспертами в соответствии с последними тенденциями в индустрии. Независимо от вашего уровня подготовки или целей, у нас есть программы, чтобы помочь вам реализовать свой потенциал</p>
      </div>
      <img src="@/assets/img/Дизайн без названия (18) 2 (1).png" alt="" class="main__info-img">
    </div>
    <div class="main__forms">
      <h2 class="main__forms-title">Удобный формат обучения</h2>
      <div class="main__content-forms  container-fluid">
      <div class="main__forms-forms" v-for="(img, idx) of image" :key="idx">
        <img
         :src="`/src/assets/img/${img.img}.png`" alt="" 
         class="main__forms-image">
         <div class="main__forms-links">
        <router-link :to="img" class="main__forms-text"> {{ img.text }} </router-link>
        </div>
      </div>
    </div>
    </div>
    <div class="main__working container-fluid">
      <div class="main__working-coworking">
        <h3 class="main__coworking-title">Коворкинг</h3>
        <p class="main__coworking-text">Коворкинг - это кабинет, оборудованный всем необходимым для того, чтобы наши студенты могли приходить практиковаться дополнительно и выполнять домашнюю работу под чутким наблюдением опытных администраторов.</p>
      </div>
      <img src="../assets/img/WEBSTEP (7) 1 (1).png" alt="" class="mian__working-img">
    </div>
    <div class="main__anketa ">
      <div class="main__anketa-anketa container">
      <h2 class="main__anketa__title">БЕСПЛАТНЫЙ ОТКРЫТЫЙ УРОК</h2>
      <div class="main__content-anketa">
      <div class="main__anketa-info">
        <p class="main__anketa-text">Перед стартом каждого курса проводятся бесплатные открытые уроки, на которых вы получите всю подробную информацию об обучении, познакомитесь с преподавателем и сможете записаться</p>
        <img src="../assets/img/anketa.png" alt="" class="main__anketa-image">
        <p class="main__anketa-zapolniy">Заполни анкету по братски</p>
      </div>
      <form class="main__contact">
        <h3 class="main__contact-title">ЗАПОЛНИТЕ АНКЕТУ</h3>
        <div class="main__contact-button">
        <input type="text" placeholder="Имя Фамилия" class="main__contact-inp">
      </div>
      <div class="main__contact-button">
        <input type="text" placeholder="Номер телефона" class="main__contact-inp">
      </div>
      <div class="main__contact-button">
        <input type="text" placeholder="Выбор курса" class="main__contact-inp">
      </div>
        <button class="main__contact-btn">Оставить заявку</button>
      </form>
    </div>
    </div>
  </div>
  </div>
</template>

<style lang="scss" scoped>
.main {


  &__info-content {
    display: flex;
    align-items: center;
    flex-wrap: wrap;
  }

  &__content {
    display: flex;
    flex-direction: column;
    align-items: center;
    width: calc(100% / 3);
    background: linear-gradient(257.65deg, #1B263B -171.23%, #415A77 79.52%);
  }

  &__content-image {
    width: 270px;
    height: 244px;  
    object-fit: contain;
  }

  &__content-text {
    padding-bottom: 37px;
    font-weight: 700;
    font-size: 30px;
    line-height: 35px;
    color: #fff;
  }

  &__info {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 130px 0 ;
    position: relative;
  }

  &__info-title {
    font-weight: 700;
    font-size: 70px;
    line-height: 75px;
    color: #474f5f;
    padding-bottom: 28px;
  }

  &__info-text {
    width: 1000px;
    font-weight: 400;
    font-size: 30px;
    color: #1B263B;
    line-height: 55px;
  }

  &__info-img {
    position: absolute;
    right: 0;
    top: -20%;
  }

  &__forms {
    padding: 140px 0;
    background: linear-gradient(270deg, #415a77 -32.97%, #1b263b 92.7%);
  }

  &__forms-title {
    text-align: center;
    font-weight: 700;
    font-size: 70px;
    line-height: 75px;
    color: #fff;
    padding-bottom: 140px;
  }

  &__content-forms {
    display: flex;
    align-items: center;
    justify-content: center;
  }

  &__forms-image {
    padding-bottom: 24px;
    object-fit: cover;
  }

  &__forms-links {
    text-align: center;
  }

  &__forms-text {
    font-weight: 700;
    font-size: 30px;
    line-height: 35px;
    color: #fff;
  }

  &__working {
    display: flex;
    align-items: center;
    gap: 98px;
    padding: 15px 0 50px 0;
  }

  &__coworking-title {
    font-weight: 700;
    font-size: 60px;
    line-height: 75px;
    color: #1B263B;
    padding-bottom: 16px;
  }

  &__coworking-text {
    width: 700px;
    font-weight: 400;
    font-size: 30px;
    line-height: 50px;
    color: #1B263B;
  }

  &__anketa {
    background: linear-gradient(270deg, #415a77 -32.97%, #1b263b 92.7%);
    padding: 100px 0 0 0;
  }

  &__anketa__title {
    font-weight: 700;
    font-size: 70px;
    line-height: 75px;
    color: #fff;
    padding-bottom: 75px;
  }

  &__anketa-info {
    position: relative;
  }

  &__anketa-text {
    width: 530px;
    font-weight: 300;
    font-size: 25px;
    line-height: 50px;
    color: #fff;
  }

  &__anketa-image {
    position: absolute;
    top: 40%;
    left: 0;
  }

  &__anketa-zapolniy {
    position: absolute;
    top: 68%;
    right: 42%;
    font-size: 25px;
    line-height: 30px;
    color: #1B263B;
    width: 200px;
    text-align: center;
  }

  &__content-anketa {
    display: flex;
    gap: 90px;
  }

  &__contact {
    padding: 50px 70px 170px 60px;
    box-shadow: 0px 4px 50px 0px #00000040;
    background: linear-gradient(264.26deg, rgba(27, 38, 59, 0.3) 2.59%, rgba(65, 90, 119, 0.3) 102.43%);
    border-radius: 20px 20px 0 0 ;
  }

  &__contact-title {
    font-weight: 700;
    font-size: 35px;
    line-height: 75px;
    color: #fff;
    padding-bottom: 22px;
  }

  &__contact-inp {
    margin-bottom: 22px;
    padding: 15px 200px 15px 50px;
    border-radius: 10px;
    background: linear-gradient(264.26deg, rgba(91, 126, 164, 0.285) 102.43%, rgba(255, 255, 255, 0.279) 2.59%,);
    border: none;

    &::placeholder {
      font-weight: 300;
      font-size: 20px;
      line-height: 50px;
      color: #fff;
    }
  }

  &__contact-btn {
    padding: 18px;
    border-radius: 10px;
    border: none;
    font-weight: 600;
    font-size: 20px;
    color: #1B263B;
  }
}
</style>
