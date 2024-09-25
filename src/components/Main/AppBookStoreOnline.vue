<script>
    import LogoContainer from './LogoContainer.vue';
    import RealStories from './RealStories.vue';

    export default {
        components: {
            LogoContainer,
            RealStories
        },
        data() {
            return {
                clientLogos: [
                    {logo: '/img/client-logo-01-primary.png'},
                    {logo: '/img/client-logo-02-primary.png'},
                    {logo: '/img/client-logo-03-primary.png'},
                    {logo: '/img/client-logo-04-primary.png'},
                    {logo: '/img/client-logo-05-primary.png'},
                    {logo: '/img/client-logo-06-primary.png'}
                ]
            }
        }
    }
</script>

<template>
    <div class="container-book-store centered">
        <div class="bookstore-online">
            <div class="bookstore-title">
                book store online
            </div>
            <div class="book-promo-title">
                Be Alpha With Wingman's Book
            </div>
            <div class="book-features">
                <ul>
                    <li class="feature-item">
                        <i class="fas fa-check"></i> Help you understand
                    </li>
                    <li class="feature-item">
                        <i class="fas fa-check"></i> Revealing mature tips
                    </li>
                    <li class="feature-item">
                        <i class="fas fa-check"></i> Give the right advice
                    </li>
                    <li class="feature-item">
                        <i class="fas fa-check"></i> Fascinating examples of alpha man
                    </li>
                </ul>
            </div>
            <button class="ebook-button" type="">Get Free Ebook</button>
        </div>
        <div class="double-card">
            <div class="card-item">
                <div class="book-image">
                    <img src="/img/product-book-11-400x400.jpg" alt="">
                </div>
                <div class="book-title">
                    Alpha man by Maxcoach
                </div>
                <div class="book-price">
                    29.00$
                </div>
            </div>
            <div class="card-item">
                <div class="book-image">
                    <img src="/img/product-book-10-400x400.jpg" alt="">
                </div>
                <div class="book-title">
                    Real man 4.0 by Maxcoach
                </div>
                <div class="book-price">
                    39.00$
                </div>
            </div>
        </div>
    </div>
    <div class="centered logo-container">
        <LogoContainer v-for="(logo, i) in clientLogos" :key="i" :logos="logo.logo" />
    </div>
    <div class="bg-img">
        <RealStories />
    </div>
</template>

<style scoped>
    .container-book-store {
        display: flex;
        margin-top: 30px;
        gap: 30px;
    }

    .bookstore-online {
        width: 40%;
        display: flex;
        flex-direction: column;
        gap: 20px;
    }

    .bookstore-title {
        font-size: 2em;
    }

    .book-promo-title {
        font-size: 3em;
    }

    .book-features {}

    ul {
        display: flex;
        gap: 10px;
        flex-direction: column;
        margin-top: 40px;
    }

    .feature-item {
        list-style-type: none;
    }

    .ebook-button {
        padding: 10px;
        background-color: rgb(52, 169, 154);
        color: white;
        width: 40%;
    }

    .double-card {
        display: flex;
        width: 60%;
    }

    .card-item {
        display: flex;
        flex-direction: column;
        text-align: center;
        gap: 10px;
    }

    .book-image {
        max-width: 400px;
        height: auto;
    }

    img {
        height: 100%;
        width: 100%;
    }

    .book-title {}

    .book-price {}

    .bg-img {
        background-image: url('/img/background-pattern-wavify.png');
        background-position: center;
        min-height: 500px;
        display: flex;
        background-color: rgb(239, 239, 246);
    }

    .logo-container {
        margin-top: 30px;
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin-bottom: 60px;
    }

    .real-stories-container {
        margin-top: 20px;
    }
</style>
