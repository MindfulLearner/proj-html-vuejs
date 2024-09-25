<script>
    import AppHeaderJumbotron from "./AppHeaderJumbotron.vue"
    import AppHeaderNumberInfo from "./AppHeaderNumberInfo.vue"
    export default {
        data() {
            return {
                listIcon: [
                    'fab fa-facebook',
                    'fab fa-twitter',
                    'fab fa-instagram',
                    'fab fa-linkedin'
                ],
                listHeader: [
                    {name: 'Home', isOpen: false, items: ['MaxCoach Education', 'Course Portal', 'Distant Learning', 'Multimedia Pedagogy', 'Modern Schooling', 'Remote Training', 'Health Coaching', 'Gym Coaching', 'Business', 'Artist', 'Kitchen Coach', 'Motivation', 'Dancing', 'Guitar', 'Yoga', 'Photography', 'Personal Finance', 'Sales Coaching', 'Mental Therapy']},
                    {name: 'Pages', isOpen: false, items: ['Start Here', 'Success Story', 'About me', 'About us 01', 'About us 02', 'About us 03', 'Contact me', 'Contact us', 'Purchase Guide', 'Privacy Policy', 'Terms of Service']},
                    {name: 'Courses', isOpen: false, items: ['Courses Grid 01', 'Courses Grid 02', 'Courses Grid 03', 'Membership Levels', 'Become a Teacher', 'Profile', 'Checkout', 'Single Layout']},
                    {name: 'Features', isOpen: false, items: ['Events', 'Zoom Meetings']},
                    {name: 'Blog', isOpen: false, items: ['swag']},
                    {name: 'Shop', isOpen: false, items: ['swag']}
                ]
            }
        },
        methods: {
            toggleDropdown(index) {
                this.listHeader[index].isOpen = !this.listHeader[index].isOpen;
            }
        },
        components: {
            AppHeaderJumbotron,
            AppHeaderNumberInfo
        }
    }
</script>

<template>
    <div class="bg-img">
        <div class="header-container centered">
            <div class="logo-container">
                <div class="img-container">
                    <img src="/img/dark-logo.png" alt="logo">
                </div>
            </div>
            <div class="list-header-container">
                <div v-for="(header, index) in listHeader" :key="index" class="menu-item">
                    <span @click="toggleDropdown(index)">
                        {{ header.name }}
                        <i class="fas fa-chevron-down"></i>
                    </span>
                    <div v-if="header.isOpen && header.items.length" class="dropdown-menu">
                        <ul>
                            <li v-for="(item, i) in header.items" :key="i">{{ item }}</li>
                        </ul>
                    </div>
                </div>
            </div>
            <div class="ul-container">
                <ul>
                    <li v-for="(icon, i) in listIcon" :key="i">
                        <i :class="icon"></i>
                    </li>
                    <div>
                        <i class="fas fa-bars hamburger"></i>
                    </div>
                </ul>
            </div>
        </div>
        <AppHeaderJumbotron />
    </div>
    <AppHeaderNumberInfo />
</template>

<style scoped>
    .dropdown-menu>ul {
        display: flex;
        flex-direction: column;
    }

    img {
        width: 100%;
        height: 100%;
    }

    .logo-container {
        width: 25%;
    }

    .list-header-container {
        gap: 45px;
        display: flex;
        justify-content: center;
        align-items: center;
        width: calc(100% - 50%);
        height: 100%;
    }

    .menu-item {
        position: relative;
    }

    .list-header-container>div {
        display: flex;
        flex-direction: column;
        align-items: center;
    }

    .header-container {
        height: 100px;
        display: flex;
        align-items: center;
        justify-content: space-between;
    }

    .ul-container {
        width: 25%;
    }

    ul {
        list-style-type: none;
        gap: 10px;
        display: flex;
        justify-content: end;
        align-items: center;
        height: 100%;
    }

    li {
        display: flex;
        align-items: center;
    }

    li>i {
        font-size: 20px;
    }

    .img-container {
        width: 150px;
        height: auto;
        display: flex;
    }

    .bg-img {
        background-image: url('/img/background-pattern-wavify.png');
        background-position: center;
        min-height: 500px;
        background-color: rgb(239, 239, 246);
    }

    .dropdown-menu {
        position: absolute;
        top: 100%;
        left: 0;
        background-color: white;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        padding: 10px;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .dropdown-menu ul {
        list-style-type: none;
        padding: 0;
        margin: 0;
    }

    .dropdown-menu li {
        padding: 5px 10px;
        white-space: nowrap;
    }
</style>
