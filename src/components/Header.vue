<template>
    <header class="header">
        <div class="header__nav">
            <img src="../assets/logo1.svg" alt="" class="nav__logo">
            <div class="nav__menu">
                <div class="nav__links">
                    <a href='/' class="nav__link">Икра</a>
                    <a href='/' class="nav__link">Рыба</a>
                    <a href='/' class="nav__link">Наши преимущества</a>
                    <a href='/' class="nav__link">Контакты</a>
                </div>
                <div class="nav__empty"></div>
                <a class="nav__phone" href="mailto:+79831292990">+7 (983) 129 29 90</a>
            </div>
        </div>
        <div class="header__contacts">
            <a href="" class="contacts__link"><img src="../assets/Ватсапп.svg" alt=""></a>
            <a href="" class="contacts__link"><img src="../assets/Корзина.svg" alt=""></a>
        </div>
    </header>
</template>


<script>
export default {
    name: 'TheHeader',
}
</script>

<style scoped>
.header {
    width: 89%;
    margin: 0 auto;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    top: 20px;
    left: 0;
    right: 0;
    z-index: 1;
}

.header__nav {
    display: flex;
    align-items: center;
    justify-content: center;
}

.nav__menu {
    position: relative;
    left: -15px;
    z-index: 1;
}

.nav__logo {
    position: relative;
    z-index: 2;
}

.nav__empty {
    background: #fff;
    height: 7px;
}

.nav__links {
    background: rgba(252, 191, 73, 0.85);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 18px;
    height: 32px;
    padding-left: 19px;
    padding-right: 19px;

}

.nav__link {
    font-weight: 700;
    font-size: 16px;
    line-height: 18px;
    color: #fff;
}

.nav__phone {
    background: rgba(252, 191, 73, 0.85);
    font-weight: 700;
    font-size: 16px;
    line-height: 18px;
    color: #fff;
    padding-left: 19px;
    padding-right: 19px;
    height: 29px;
}

.header__contacts {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 7px;
}

.contacts__link {
    width: 53px;
    height: 53px;
}

@media screen and (max-width: 767px) {
    .nav__menu {
        display: none;
    }

    .nav__logo {
        max-width: 65px;
        max-height: 65px;
    }
}
</style>