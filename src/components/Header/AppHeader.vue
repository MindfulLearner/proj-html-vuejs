<script>
    import AppHeaderJumbotron from "./AppHeaderJumbotron.vue"
    import AppHeaderNumberInfo from "./AppHeaderNumberInfo.vue"
    export default {
        data() {
            return {
                listIcon: [
                    'fab fa-facebook',
                    'fab fa-twitter',
                    'fab fa-instagram',
                    'fab fa-linkedin'
                ],
                listHeader: [
                    'Home',
                    'Pages',
                    'Courses',
                    'Features',
                    'Blog',
                    'Shop',
                ]
            }
        },
        components: {
            AppHeaderJumbotron,
            AppHeaderNumberInfo
        }
    }
</script>
<template>
    <div class="bg-img">
        <div class="header-container centered">
            <div class="logo-container">
                <div class="img-container">
                    <img src="/img/dark-logo.png" alt="">
                </div>
            </div>
            <div class="list-header-container">
                <div v-for="(a, i) in listHeader">
                    {{ a }}
                    <i class="fas fa-chevron-down"></i>
                </div>
            </div>
            <div class="ul-container">
                <ul>
                    <li v-for="(icon, i) in listIcon" :key="i">
                        <i :class="icon"></i>
                    </li>
                    <div>
                        <i class="fas fa-bars hamburger"></i>
                    </div>
                </ul>
            </div>
        </div>
        <AppHeaderJumbotron />
        <AppHeaderNumberInfo />
    </div>
</template>

<style scoped>
    img {
        width: 100%;
        height: 100%;
    }

    .logo-container {
        width: 25%;
    }

    .list-header-container {
        gap: 45px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: calc(100% - 50%);
        height: 100%;
    }

    .list-header-container>div {
        display: flex;
    }

    .header-container {
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .hamburger {}

    .ul-container {
        width: 25%;
    }

    ul {
        listIcon-style-type: none;
        gap: 10px;
        display: flex;
        justify-content: end;
        align-items: center;
        height: 100%;
    }

    li {
        display: flex;
        align-items: center;
    }

    li>i {
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
        min-height: 500px;
    }
</style>
