<template>
    <div class="catalog__element" v-for="item in red" :key="item">
        <h2 class="element__title">{{ item.title }}</h2>
        <img :src="item.image" :alt="item.title" class="element__image">
        <div class="element__text">
            <p class="element__description">{{ item.description }}</p>
            <p class="element__quality">Качество: <img src="../assets/звездочки.svg" alt="звездочки"></p>
            <p class="element__weight">{{ item.weight }}</p>
            <p class="element__price">Стоимость: {{ item.price }}</p>
        </div>
        <button class="element__about">Подробнее</button>
        <div class="element__buttons">
            <button class="element__tostash">В корзину</button>
            <button class="element__buy">Купить</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TheItem',
    props: ['red'],

}
</script>

<style scoped>
.catalog__element {
    max-width: 292px;
    width: 100%;
    background: rgba(6, 8, 11, 0.56);
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    color: #fff;
    font-weight: 500;
    font-size: 20px;
    line-height: 22px;
}

.element__title {
    font-weight: 700;
    font-size: 20px;
    line-height: 22px;
    text-align: center;
}

.element__image {
    max-width: 229px;
    max-height: 232px;
}

.element__about {
    background: #D9D1BD;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 3px;
    max-width: 196px;
    width: 100%;
    text-align: center;
    font-weight: 500;
    font-size: 18px;
    line-height: 20px;
    color: #393939;
    margin-bottom: 17px;
    height: 26px;
    margin-top: 22px;
}

.element__buttons {
    max-width: 264px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 6px;
    margin-bottom: 46px;
}

.element__tostash {
    font-weight: 500;
    font-size: 18px;
    line-height: 20px;
    text-align: center;
    color: #393939;
    max-width: 129px;
    width: 100%;
    height: 42px;
    background: linear-gradient(360deg, rgba(0, 0, 0, 0.2) 0%, rgba(0, 0, 0, 0) 50%, rgba(0, 0, 0, 0.179167) 100%), #D9D1BD;
    border: 1px solid #EB6B36;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 3px;
}

.element__buy {
    max-width: 129px;
    width: 100%;
    height: 42px;
    font-weight: 500;
    font-size: 18px;
    line-height: 20px;
    text-align: center;
    color: #393939;
    background: rgba(235, 107, 54, 0.95);
    border: 1px solid #D9D1BD;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    border-radius: 3px;
}

.element__quality {
    display: flex;
    align-items: center;
    justify-content: center;
}

.element__text {
    max-width: 254px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    text-align: center;
}
</style>