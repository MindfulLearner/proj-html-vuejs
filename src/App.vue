<script>
    import AppHeader from './components/Header/AppHeader.vue';
    import AppFooter from './components/Footer/AppFooter.vue';
    import AppMainJumbotron from './components/Main/AppMainJumbotron.vue';

    export default {
        components: {
            AppHeader,
            AppFooter,
            AppMainJumbotron
        },
    };
</script>
<template>
    <div>
        <AppHeader />
        <AppMainJumbotron />
        <AppFooter />
    </div>
</template>
<script scoped>

</script>
