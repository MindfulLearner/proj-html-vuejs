<script>
    export default {
        data() {
            return {
                aboutMe: "About me",
                alphaMaleTitle: "How to Be an Alpha Male: The 15 Habits of True Alphas",
                businessGoal: "Your goal is to show the consistency of business, core values, and customer care. Punctuality, responsibility, individuality, accuracy, enthusiasm – you have to clearly explain how these qualities are applicable to your work. And the important thing is you do love what you do.",
                learnAlphaMale: "Want to learn how to be an alpha male? How to be more masculine? How to be the man you’ve always wanted to be?",
                textCitazione: "Every morning you have two choices: continue to sleep with your dreams, or wake up and chase them.",
                kaixa: "Kaixa Stark",
                wingman: "Wingman"
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
                {{ learnAlphaMale }}
            </div>
            <div class="learn-alpha-male">
                {{ businessGoal }}
            </div>
        </div>
    </div>
    <div class="container centered">
        <div class="container-video">
            <iframe src="https://www.youtube.com/embed/ElFJ1qcl74U"
                title="Easily Customize Your Coaching Site With Elementor &amp; MaxCoach" frameborder="0"
                allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
                referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
        <div class="container-video-text">
            <div class="text-citazione">
                {{ textCitazione }}
            </div>
            <div class="container-shape-img">
                <img src="/img/home-movation-shape-01.png" alt="">
            </div>
            <div class="kaixa-text">
                {{ kaixa }}
            </div>
            <div class="wingman-text">
                {{ wingman }}
            </div>
        </div>
    </div>
</template>

<style scoped>
    .text-citazione {
        font-size: 2em;
        margin-bottom: 30px;
    }

    .container-video {
        width: 60%;

        >img {
            width: 100%;
            height: 100%;
        }
    }

    .container-video-text {
        width: 40%;
        padding-left: 20px;
        padding-top: 50px;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    iframe {
        width: 100%;
        height: 100%;
    }

    .container-shape-img {
        width: 2em;
        height: 20px;

        img {
            width: 100%;
            height: 100%;
        }
    }

    .container {
        display: flex;
        margin-top: 50px;
    }

    .abt-me-container,
    .business-goal-container {
        display: flex;
        flex-direction: column;
        width: 50%;
        gap: 20px;
    }

    .business-goal-container {
        padding-top: 45px;
    }

    .about-me {
        width: 50%;
        color: rgb(36, 173, 151);
        font-size: 2em;
    }

    .alpha-male-title {
        width: 80%;
        font-weight: bold;
        font-size: 3em;
    }

    .business-goal {}

    .learn-alpha-male {}
</style>
