<template>
    <div class="cargo">
        <img src="../assets/корзина.png" alt="" class="cargo__title">
        <div class="cargo__content">
            <div class="cargo__element" v-for="item in items" :key="item">
                <img :src="item.image" :alt="item.title" class="element__image">
                <p class="element__title">{{ item.title }}</p>
                <div class="element__amount">
                    <img src="../assets/arrowup.svg" alt="arrow" class="amount__arrow arrow" @click="moreAmount">
                    <p class="amount__number">{{ item.amount }}</p>
                    <img src="../assets/arrowdown.svg" alt="arrow" class="amount__arrow arrow" @click="lessAmount">
                </div>
                <div class="element__price">
                    <p class="price__title">Стоимость</p>
                    <p class="price__amount">{{ item.price }}</p>
                </div>
            </div>
            <p class="cargo__amount">Итого: <span class="cargo__amount-span">{{ allprice }}</span></p>
            <button class="cargo__buy">Купить</button>
        </div>
    </div>
</template>

<style scoped>
.arrow {
    cursor: pointer;
}

.cargo {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    z-index: 99999999999;
    position: fixed;
    right: 56px;
    top: 100px;
}

.cargo__content {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    background: rgba(15, 15, 15, 0.8);
    border-radius: 6px;
    max-width: 411px;
    width: 100%;
}

.cargo__element {
    max-width: 366px;
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 16px;
    font-weight: 500;
    font-size: 14px;
    line-height: 16px;
    color: #fff;
    background: url('../assets/текстуракорзина.png');
}

.element__image {
    max-width: 61px;
    max-height: 56px;
}

.element__title {
    font-weight: 700;
    font-size: 14px;
    line-height: 16px;
    text-align: center;
    color: #FFFFFF;
    max-width: 110px;
    width: 100%;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 42px;
    background: rgba(0, 0, 0, 0.43);
    border-radius: 10px;
}

.element__amount {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
}

.price__amount {
    background: rgba(0, 0, 0, 0.43);
    border-radius: 10px;
    max-width: 70px;
    width: 100%;
    height: 28px;
    display: flex;
    align-items: center;
    justify-content: center;
    margin-top: 6px;
}
</style>
<script>
export default {
    name: 'TheCargo',
    data() {
        return {
            allprice: 0,
            items: [
                {
                    title: 'Икра Кижуч 250 гр',
                    amount: 1,
                    price: 15000,
                    image: require('../assets/кижуч.png'),
                }
            ]
        }
    },
    methods: {
        moreAmount() {
        }
    }
}
</script>