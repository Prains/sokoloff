<template>
    <section class="contact">
        <div class="contact__lead">
            <img src="../assets/bottomlogo.svg" alt="" class="lead__img">
            <h2 class="lead__title">Контактная информация</h2>
            <img src="../assets/bottomlogo.svg" alt="" class="lead__img">
        </div>
        <div class="contact__content">
            <div></div>
            <p class="contact__text">
                Самовывоз из нашего офиса по адресу:
                г. Новосибирск, ул. Ломоносова 55/1
                (предварительно бронируйте заказ).
                <br>
                <br>
                Цены на сайте могут отличаться от цен в магазине.
                <br>
                * Бесплатная доставка красной икры от 1 кг.
                <br>
                <br>
                Отзывы о работе компании и предложения отправляйте на почту: sasha@sokoloff-fish.ru
                <br>
                Телефон: +7 (983) 129 29 90
            </p>
            <img src="../assets/Ватсапп.svg" alt="" class="">
        </div>
    </section>
</template>

<script>
export default {
    name: 'TheContacts',
}
</script>

<style scoped>
.contact__lead {
    width: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: 63px;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0.2) 21.35%, rgba(0, 0, 0, 0.0382353) 50.52%, rgba(0, 0, 0, 0) 97.4%), rgba(252, 191, 73, 0.94);
}

.lead__title {
    margin: 0;
    font-weight: 700;
    font-size: 36px;
    line-height: 40px;
    text-align: center;
    color: #fff;
}

.contact__content {
    background: url('../assets/bottomfish.png') no-repeat;
    background-size: cover;
    height: 501px;
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-direction: column;
}

.contact__text {
    font-weight: 700;
    font-size: 24px;
    line-height: 27px;
    text-align: center;
    color: #fff;
}

@media screen and (max-width: 767px) {
    .lead__img {
        max-width: 65px;

    }

    .lead__title {
        font-size: 18px;
        line-height: 20px;
    }
}
</style>