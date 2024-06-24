<template>
<footer class="footer">
    <div class="footer__content container">
    <h3 class="footer__content-title">Работать нужно не 12 часов, а головой</h3>
    <div class="footer__content-contactes">
        <p class="footer__contactes-num"> +998 88 800 88 98</p>
    <div class="footer__contactes-image">
        <img src="../../assets/img/telegram-fill-svgrepo-com 1.png" alt="" class="footer__content-img">
    </div>
    <div class="footer__contactes-image">
        <img src="../../assets/img/facebook-svgrepo-com 1.png" alt="" class="footer__content-img">
    </div>
    <div class="footer__contactes-image">
        <img src="../../assets/img/Group 18.png" alt="" class="footer__content-img">
    </div>
    </div>
</div>
</footer>
</template>

<style lang="scss" scoped>
.footer {
    &__content {
        padding: 125px 0 65px 0;

        &-title {
            font-weight: 700;
            font-size: 60px;
            line-height: 75px;
            color: #1B263B;
        }

        &-contactes {
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 7px;
            padding-top: 30px;
        }
}

    &__contactes-num {
        font-weight: 600;
        font-size: 45px;
        line-height: 75px;
        color: #1B263B;
        padding-right: 40px;
    }

    &__contactes-image {
        display: flex;
        align-items: center;
        justify-content: center;
    }
    
}
</style>