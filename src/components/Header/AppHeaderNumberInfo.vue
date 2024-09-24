<script>
    export default {
        data() {
            return {
                dati: [
                    {number: "1.926", paragraph: "Finished Sessions"},
                    {number: "100%", paragraph: "Satisfaction rate"},
                    {number: "3092+", paragraph: "ENROLLED LEARNERS"},
                    {number: "200", paragraph: "Online Instructors"}
                ]
            }
        }
    }
</script>

<template>
    <div class="container-info centered">
        <div class="card-info" v-for="(item, index) in dati" :key="index">
            <div class="number">
                {{ item.number }}
            </div>
            <div class="paragraph">
                {{ item.paragraph }}
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container-info {
        margin-top: 50px;
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }

    .card-info {
        width: calc((100% / 4) - 15px);
        padding: 20px;
        text-align: center;
        border-left: 1px dashed rgb(36, 173, 151);
    }

    .number {
        color: rgb(36, 173, 151);
        font-size: 2em;
        font-weight: bold;
    }

    .paragraph {
        margin-top: 10px;
        font-size: 1.2em;
    }
</style>
