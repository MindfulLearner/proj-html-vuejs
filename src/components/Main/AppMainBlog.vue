<script>
    import cardMainBlog from './cardMainBlog.vue';

    export default {
        components: {
            cardMainBlog
        },
        data() {
            return {
                blogUpdated: 'Blog Updated',
                articlesUpdated: 'Interesting articles updated daily',
                cards: [
                    {data: 'May 13, 2020', titoloCarders: 'How to Stay True to Your Personal Brand', descrizione: 'When it comes to your business or career, you want …', imgSrc: '/img/motivation-blog-01-480x325.jpg'},
                    {data: 'May 13, 2020', titoloCarders: '5 Vital Lessons in 5 Years of Freelancing', descrizione: 'Being self-employed and working from home, it’s easy to get …', imgSrc: '/img/motivation-blog-02-480x325.jpg'},
                    {data: 'May 13, 2020', titoloCarders: '11 Super Useful Tips for Small-Business Owners', descrizione: 'Being a small-business owner poses a ton of challenges. We …', imgSrc: '/img/motivation-blog-03-480x325.jpg'},
                    {data: 'May 13, 2020', titoloCarders: 'How to Give Yourself Grace to Start Again', descrizione: 'Forgive yourself for bad habits you may have started or …', imgSrc: '/img/motivation-blog-04-480x325.jpg'}
                ]
            };
        }
    };
</script>

<template>
    <div class="container-blog-updated centered">
        <div class="blog-updated">
            {{ blogUpdated }}
        </div>
        <div class="articles-updated">
            {{ articlesUpdated }}
        </div>
    </div>
    <div class="centered">
        <cardMainBlog v-for="(card, i) in cards" :key="i" :data="card.data" :titoloCarders="card.titoloCarders"
            :descrizione="card.descrizione" :imgSrc="card.imgSrc" />
    </div>
    <div class="view">
        VIEW ALL POSTS
    </div>
</template>

<style scoped>
    .view {
        display: flex;
        justify-content: center;
        text-align: center;
        color: rgb(52, 169, 154);
    }

    .centered {
        display: flex;
        flex-wrap: wrap;
        gap: 20px;
    }

    .container-blog-updated {
        display: flex;
        flex-direction: column;
        gap: 30px;
        justify-content: center;
        align-content: center;
        text-align: center;
        margin-top: 50px;
        margin-bottom: 50px;
    }

    .blog-updated {
        font-size: 2em;
        font-weight: bold;
        color: #333;
    }

    .articles-updated {
        font-size: 1.2em;
        font-weight: 400;
        color: grey;
    }
</style>
