<script>
    export default {
        props: {
            logos: {
                type: String,
            }
        }
    }
</script>
<template>
    <div class="client-logo-container">
        <div class="client-logo">
            <img :src="logos" alt="Client Logo">
        </div>
    </div>
</template>



<style scoped>
    .client-logo-container {
        width: calc((100% / 6) - 9px);
    }

    .client-logo {
        height: 100px;
    }

    img {
        width: 100%;
        height: 100%;
    }
</style>
