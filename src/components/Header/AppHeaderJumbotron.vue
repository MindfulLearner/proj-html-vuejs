<script>
    export default {
        data() {
            return {

            }
        }
    }
</script>
<template>
    <div class="container centered">
        <div class="wingman-container">
            <div class="wingman-title">
                I'm WINGMAN
            </div>
            <h1 class="wingman-heading">Peace On Earth A Wonderful Wish But No Way</h1>
            <p class="wingman-description">
                Success isn’t overnight. It’s when every day you get a little better than the day before. It all adds
                up.
            </p>
            <button class="wingman-button" type="">Get Started For Free</button>
        </div>
        <div class="wingman-image-container">
            <div class="wingman-image-wrapper">
                <img class="wingman-image" src="/img/home-movation-hero-image.png" alt="">
            </div>
        </div>
    </div>
</template>
<style scoped>
    .container {
        display: flex;
        margin-top: 80px;
        gap: 10px;
    }

    .wingman-container {
        display: flex;
        flex-direction: column;
        gap: 40px;
        padding-top: 120px;
    }

    .wingman-title {
        width: 60%;
    }

    .wingman-heading {
        width: 60%;
    }

    .wingman-description {
        width: 60%
    }

    .wingman-button {
        width: 30%;
        padding: 20px;
        color: white;
        background-color: rgb(36, 173, 151);
    }

    .wingman-button:hover {
        background-color: rgb(63, 58, 100);
    }

    .wingman-image-container {
        background-image: url(/img/home-movation-shape-face.png);
    }

    .wingman-image-wrapper {}

    .wingman-image {}
</style>
