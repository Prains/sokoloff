<template>
    <section class="advantage">
        <div class="advantage__topsection">
            <h2 class="advantage__title">
                Наши преимущества
            </h2>
        </div>
        <div class="advantage__elements">
            <div class="element" v-for="card in cards" :key="card">
                <img :src="card.background" :alt="card.title" class="element__img">
                <div class="element__lead">
                    <h2 class="element__title">{{ card.title }}</h2>
                </div>
            </div>
        </div>
        <div class="advantage__bottomsection">

        </div>
    </section>
</template>

<script>
export default {
    name: 'TheAdvantage',
    data() {
        return {
            cards: [
                {
                    background: require('../assets/kam.png'),
                    title: 'Напрямую с Камчатки'
                },
                {
                    background: require('../assets/deg.png'),
                    title: 'Бесплатная дегустация',
                },
                {
                    background: require('../assets/payment.png'),
                    title: 'Оплата после получения',
                },
                {
                    background: require('../assets/delivery.png'),
                    title: 'Бесплатная доставка',
                }
            ]
        }
    }
}
</script>

<style scoped>
.advantage__topsection {
    width: 100%;
    background: linear-gradient(180deg, rgba(0, 0, 0, 0.2) 21.03%, rgba(0, 0, 0, 0.13058) 61.87%, rgba(0, 0, 0, 0) 100%), #FCBF49;
    height: 145px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.advantage__bottomsection {
    background: linear-gradient(209.41deg, rgba(0, 0, 0, 0) 35.65%, rgba(0, 0, 0, 0.2) 68.53%), #FCBF49;
    height: 38px;
}

.advantage__title {
    margin: 0;
    font-weight: 700;
    font-size: 36px;
    line-height: 40px;
    color: #fff;
    text-align: center;
}

.advantage__elements {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
}

@media screen and (max-width:767px) {
    .advantage__elements {
        grid-template-columns: 1fr;
    }
}

.element {
    position: relative;
    height: 623px;
    width: 100%;
}

.element:hover {
    -webkit-box-shadow: 1px 0px 100px 13px rgba(34, 60, 80, 1);
    -moz-box-shadow: 1px 0px 100px 13px rgba(34, 60, 80, 1);
    box-shadow: 1px 0px 100px 13px rgba(34, 60, 80, 1);
}

.element__img {
    width: 100%;
    height: 100%;
    object-fit: cover;
}

.element__lead {
    position: absolute;
    bottom: 9px;
    width: 100%;
    text-align: center;
    background: rgba(17, 23, 30, 0.65);
}

.element__title {
    color: #fff;
    font-weight: 500;
    font-size: 24px;
    line-height: 27px;
}
</style>