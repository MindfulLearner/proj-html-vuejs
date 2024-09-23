<script>
    export default {
        data() {
            return {
                aboutMe: "About me",
                alphaMaleTitle: "How to Be an Alpha Male: The 15 Habits of True Alphas",
                businessGoal: "Your goal is to show the consistency of business, core values, and customer care. Punctuality, responsibility, individuality, accuracy, enthusiasm – you have to clearly explain how these qualities are applicable to your work. And the important thing is you do love what you do.",
                learnAlphaMale: "Want to learn how to be an alpha male? How to be more masculine? How to be the man you’ve always wanted to be?"
            }
        }
    }
</script>

<template>
    <div class="container centered">
        <div class="abt-me-container">
            <div class="about-me">
                {{ aboutMe }}
            </div>
            <div class="alpha-male-title">
                {{ alphaMaleTitle }}
            </div>
        </div>
        <div class="business-goal-container">
            <div class="business-goal">
                {{ businessGoal }}
            </div>
            <div class="learn-alpha-male">
                {{ learnAlphaMale }}
            </div>
        </div>
    </div>
</template>

<style scoped>
    .container {
        display: flex;
    }

    .abt-me-container {
        display: flex;
        flex-direction: column;
        width: 50%;
    }

    .business-goal-container {
        width: 50%;
        display: flex;
        flex-direction: column;
    }

    .about-me {
        width: 50%;
    }


    .alpha-male-title {
        width: 50%;
    }

    .business-goal {}

    .learn-alpha-male {}
</style>
