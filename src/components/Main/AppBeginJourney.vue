<script>
    import Card from './Card.vue'; // Importa il componente Card

    export default {
        components: {
            Card
        },
        data() {
            return {
                beginJourney: 'Begin your journey at Maxcoach',
                latestTitle: 'Latest',
                lookAllCourses: 'Look all courses',
                cards: [
                    {costo: '$30.00', titoloCarders: 'How to be Successful: Create A Growth Mindset For Success', numerolezioni: '3 Lessons', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-01-480x298.jpg'},
                    {costo: '$30.00', titoloCarders: 'How to Build Confidence in Your Abilities', numerolezioni: '1 Lesson', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-02-480x298.jpg'},
                    {costo: '$20.00', titoloCarders: 'Productivity Machine – Focus in a Distracted World', numerolezioni: '5 Lessons', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-03-480x298.jpg'},
                    {costo: '$20.00', titoloCarders: 'Effective Time Management Mastery – Complete Guide', numerolezioni: '18 Lessons', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-04-480x298.jpg'},
                    {costo: '$25.99', titoloCarders: 'Body Language Secrets for Entrepreneurs', numerolezioni: '19 Lessons', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-05-480x298.jpg'},
                    {costo: '$19.99', titoloCarders: 'Management Skills: The Science of Leadership', numerolezioni: '17 Lessons', numerostudenti: '50 Students', imgSrc: 'img/motivation-course-06-480x298.jpg'}
                ]
            };
        }
    };
</script>

<template>
    <div class="container-begin-journey centered">
        <div class="begin-journey">
            {{ beginJourney }}
        </div>
        <div class="latest-title">
            {{ latestTitle }}
        </div>
    </div>
    <div class="centered">
        <card v-for="(card, i) in cards" :key="i" :costo="card.costo" :titoloCarders="card.titoloCarders"
            :numerolezioni="card.numerolezioni" :numerostudenti="card.numerostudenti" :imgSrc="card.imgSrc" />
    </div>
    <div class="centered swag view all the courses">
        <button type="button" class="bottone">{{ lookAllCourses }}</button>
    </div>
</template>

<style scoped>
    .centered {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }

    .swag {
        margin-top: 20px;
        display: flex;
        justify-content: center;
        align-content: center;
    }

    .bottone {
        padding: 15px;
        background-color: rgb(32, 173, 150);
        color: white;
    }

    .container-begin-journey {
        display: flex;
        flex-direction: column;
        gap: 30px;
        justify-content: center;
        align-content: center;
        text-align: center;
        margin-top: 50px;
        margin-bottom: 50px;
    }

    .begin-journey {
        font-size: 1.2em;
        font-weight: 400;
        color: grey;
    }

    .latest-title {
        font-size: 2em;
        font-weight: bold;
        color: #333;

        &::after {
            content: ' Online Courses';
            color: rgb(32, 173, 150);
            font-weight: bold;
        }
    }
</style>
