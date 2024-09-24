<script>
    export default {
        props: {
            costo: String,
            titoloCarders: String,
            numerolezioni: String,
            numerostudenti: String,
            imgSrc: String
        }
    };
</script>

<template>
    <div class="card">
        <div class="card-container">
            <img :src="imgSrc" alt="" class="course-image" />
        </div>
        <p class="card-price">{{ costo }}</p>
        <h3 class="card-title">{{ titoloCarders }}</h3>
        <div>
            <i class="fas fa-file-alt"></i>
            <p class="card-lessons">{{ numerolezioni }}</p>
            <i class="fas fa-user"></i>
            <p class="card-students">{{ numerostudenti }}</p>
        </div>
    </div>
</template>

<style scoped>
    .card>div:last-child {
        display: flex;
        gap: 10px;
        margin-top: 40px;

    }

    .card-price {
        color: rgb(32, 173, 150);
        font-size: 20px;
    }


    .crad-title {
        width: 80%;
    }

    .card {
        padding: 10px;
        width: calc((100% / 3) - 14px);
    }

    .course-image {
        width: 100%;
        height: 100%;
    }

    .card-container {
        width: 100%;
        height: auto;
    }
</style>
