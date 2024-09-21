<script>
    import AppHeaderJumbotron from "./AppHeaderJumbotron.vue"
    export default {
        data() {
            return {
                list: [
                    'fab fa-facebook',
                    'fab fa-twitter',
                    'fab fa-instagram',
                    'fab fa-linkedin'
                ]
            }
        },
        components: {
            AppHeaderJumbotron
        }
    }
</script>
<template>
    <div class="bg-img">
        <div class="header-container centered">
            <div class="img-container">
                <img src="/img/dark-logo.png" alt="">
            </div>
            <div class="ul-container">
                <ul>
                    <li v-for="(icon, i) in list" :key="i">
                        <i :class="icon"></i>
                    </li>
                    <div>
                        ciao
                    </div>
                </ul>
            </div>
        </div>
        <AppHeaderJumbotron />
    </div>
</template>

<style scoped>
    img {
        width: 100%;
        height: 100%;
    }

    .header-container {
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    ul {
        list-style-type: none;
        gap: 10px;
        display: flex;
        justify-content: end;
        align-items: center;
        width: 400px;
        height: 100%;
    }

    li {
        display: flex;
        align-items: center;
    }

    i {
        font-size: 20px;
    }

    .img-container {
        width: 150px;
        height: auto;
        display: flex;
    }

    .bg-img {
        background-image: url('/img/background-pattern-wavify.png');
        background-position: center;
        height: 500px;
    }
</style>
