<script>
    export default {
        data() {
            return {
                testimonials: [
                    {
                        image: '/img/testimonial-avata-01.jpg',
                        quote: 'I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.',
                        name: 'Mina Hollace',
                        profession: 'Freelancer'
                    },
                    {
                        image: '/img/testimonial-avata-02.jpg',
                        quote: 'I need to get a certification for English proficiency and MaxCoach is my best choice. Their tutors are smart and professional when dealing with students.',
                        name: 'Madley Pondor',
                        profession: 'IT Specialist'
                    },
                    {
                        image: '/img/testimonial-avata-03.jpg',
                        quote: 'I am happy with their arrangement of lessons and subjects. They reflect a scientific investigation into effective methods to adopt for learners.',
                        name: 'Joshuadima',
                        profession: 'Private Tutor'
                    },
                    {
                        image: '/img/testimonial-avata-04.jpg',
                        quote: 'I\'m a very strict person so I require everything to be organized and neat. Then, I\'ll be able to make things right and shine. MaxCoach guys just got me.',
                        name: 'Francesco Totti',
                        profession: 'Multimedia Admin'
                    }
                ],
                currentTestimonialIndex: 0
            }
        },
        methods: {
            nextTestimonial() {
                this.currentTestimonialIndex = (this.currentTestimonialIndex + 1) % this.testimonials.length;
            },
            previousTestimonial() {
                this.currentTestimonialIndex = (this.currentTestimonialIndex - 1 + this.testimonials.length) % this.testimonials.length;
            }
        }
    }
</script>

<template>
    <div class="container">
        <div class="caroselloswag">
            <div>
                REAL STORIES
            </div>
            <div class="quote-text">{{ testimonials[currentTestimonialIndex].quote }}</div>
            <div class="testinial-img">
                <img :src="testimonials[currentTestimonialIndex].image">
            </div>
            <div>
                {{ testimonials[currentTestimonialIndex].name }}
            </div>
            <div>{{ testimonials[currentTestimonialIndex].profession }}</div>
        </div>
        <div>
            <button @click="previousTestimonial">precedenteCarosello</button>
            <button @click="nextTestimonial">prossimoCarosello</button>
        </div>
        <div class="img-containerMax">
            <img src="/img/home-movation-testimonial-image-768x562.jpg" alt="">
        </div>
    </div>
</template>

<style scoped>
    .quote-text {
        width: 600px;
    }

    .carosello {
        width: 50%;

    }

    .caroselloswag {
        display: flex;
        flex-direction: column;
        gap: 20px;
        width: 100%;
        align-items: center;
    }

    .container {
        display: flex;
        align-items: center;
        width: 100%;
    }

    .img-containerMax {
        width: 400px;
        height: auto;

    }

    .testinial-img {
        width: 70px;
        height: 70px;
    }

    img {
        height: 100%;
        width: 100%;
    }
</style>
