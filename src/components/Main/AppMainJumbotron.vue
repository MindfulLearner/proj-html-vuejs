<script>
    import AppAboutMe from './AppAboutMe.vue'
    import AppBeginJourney from './AppBeginJourney.vue'
    import AppBookStoreOnline from './AppBookStoreOnline.vue'
    import AppMainBlog from './AppMainBlog.vue'

    export default {
        data() {
            return {

            }
        },
        components: {
            AppAboutMe,
            AppBeginJourney,
            AppBookStoreOnline,
            AppMainBlog,
        }
    }
</script>

<template>
    <AppAboutMe />
    <AppBeginJourney />
    <AppBookStoreOnline />

    <AppMainBlog />
</template>

<style scoped>
</style>
