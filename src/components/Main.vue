<template>
    <section class="main">
        <div></div>
        <div class="main__lead">
            <h1 class="main__title">Красная икра и рыба с Камчатки
            </h1>
            <p class="main__subtitle">с бесплатной доставкой по Новосибирску
            </p>
        </div>
        <img src="../assets/icondown.svg" alt="" class="icondown">
    </section>
</template>

<script>
export default {
    name: 'TheMain',
}
</script>

<style scoped>
.main {
    width: 100%;
    height: 768px;
    background: url(../assets/mainscreen.jpg) no-repeat;
    background-size: cover;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
}

.main__lead {
    width: 100%;
    text-align: center;
    background: rgba(17, 23, 30, 0.56);
    color: #fff;
}

.main__title {
    font-weight: 700;
    font-size: 36px;
    color: #FFFFFF;
    text-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
    margin: 20px 0 10px 0;
}

.main__subtitle {
    font-weight: 400;
    font-size: 20px;
    line-height: 22px;
    color: #FFFFFF;
    margin: 0 0 20px 0;
}


.mainimg {
    width: 100%;
    max-height: 768px;
}

.icondown {
    animation: move 2s infinite ease-in-out;
    width: 65px;
    height: 49px;
}

@media screen and (max-width:767px) {
    .main {
        background-position: center center;
    }
}


@keyframes move {
    0% {
        transform: translate(0, 0);
    }

    50% {
        transform: translate(0, -20px);
    }

    100% {
        transform: translate(0, 0);
    }
}
</style>