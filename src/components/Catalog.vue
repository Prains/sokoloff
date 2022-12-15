<template>
    <section class="catalog">
        <img src="../assets/текстура.svg" alt="" class="catalog__lead">
        <div class="catalog__item">
            <Item :red="red"></Item>
        </div>
        <img src="../assets/fish.png" alt="" class="catalog__lead">
        <div class="catalog__item catalog__fish">
            <item :red="fish"></item>
        </div>
    </section>
</template>
<script>
import Item from './Item.vue'
export default {
    name: 'TheCatalog',
    components: { Item },
    data() {
        return {
            red: [
                {
                    title: 'Икра Кижуч',
                    image: require('../assets/red1.png'),
                    description: 'Икра слабосоленая',
                    weight: 'Фасовка: 250гр',
                    price: '1500 руб',
                },
                {
                    title: 'Икра Кеты',
                    image: require('../assets/red2.png'),
                    description: 'Икра слабосоленая',
                    weight: 'Фасовка: 250гр',
                    price: '1500 руб'
                },
                {
                    title: 'Икра Горбуши',
                    image: require('../assets/red3.png'),
                    description: 'Икра среднесоленая',
                    weight: 'Фасовка: 250гр',
                    price: '1400 руб'
                },
            ],
            fish: [
                {
                    title: 'Кета',
                    image: require('../assets/fish1.png'),
                    description: 'Рыба свежемороженая потрошеная без головы',
                    weight: 'Фасовка: Брикет 11кг',
                    price: '650 руб/кг',
                },
                {
                    title: 'Кижуч',
                    image: require('../assets/fish2.png'),
                    description: 'Рыба свежемороженая потрошеная без головы',
                    weight: 'Фасовка: Брикет 11кг',
                    price: '650 руб/кг'
                },
                {
                    title: 'Нерка',
                    image: require('../assets/fish3.png'),
                    description: 'Рыба свежемороженая потрошеная без головы',
                    weight: 'Фасовка: Брикет 11кг',
                    price: '850 руб/кг'
                },
                {
                    title: 'Чавыча',
                    image: require('../assets/fish4.png'),
                    description: 'Рыба свежемороженая потрошеная без головы',
                    weight: 'Фасовка: Поштучно (вес 1 рыбы 5-12 кг)',
                    price: '1900 руб./ кг'
                },
            ]
        }
    }
}
</script>
<style scoped>
.catalog {
    background: url('../assets/sea.png') no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
}

.catalog__lead {
    margin-top: 13px;
    margin-bottom: 13px;
}

.catalog__item {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-wrap: wrap;
    gap: 28px;
    max-width: 1082px;
    width: 100%;
    background: url('../assets/деревяшка.png');
    object-fit: contain;
    padding-top: 14px;
    padding-bottom: 14px;
}

.catalog__fish {
    max-width: 1243px;
    gap: 9px;
    margin-bottom: 100px;
}

@media screen and (max-width: 767px) {
    .catalog__lead {
        max-width: 320px;

    }
}
</style>