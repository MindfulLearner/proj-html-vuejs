<script>
    export default {
        props: {
            data: String,
            titoloCarders: String,
            descrizione: String,
            imgSrc: String
        }
    };
</script>

<template>
    <div class="card">
        <div class="card-container">
            <img :src="imgSrc" alt="" class="blog-image" />
        </div>
        <p class="card-date">{{ data }}</p>
        <h3 class="card-title">{{ titoloCarders }}</h3>
        <p class="card-description">{{ descrizione }}</p>
    </div>
</template>

<style scoped>
    .card {
        padding: 10px;
        width: calc((100% / 4) - 15px);
        margin-bottom: 20px;
    }

    .card-container {
        width: 100%;
        height: auto;
    }

    .blog-image {
        width: 100%;
        height: auto;
    }

    .card-date {
        color: grey;
        font-size: 14px;
        margin: 10px 0;
    }

    .card-title {
        font-size: 18px;
        font-weight: bold;
        margin: 10px 0;
    }

    .card-description {
        font-size: 16px;
        color: #333;
    }
</style>
