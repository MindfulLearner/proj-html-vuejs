<script>
    export default {
        data() {
            return {
                address: '382 NE 191st St # 87394 Miami, FL 33179-3899',
                phone: '+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)',
                email: 'support@maxcoach.com',
                exploreLinks: ['Start here', 'Success story', 'Blog', 'Courses', 'About us', 'Contact us'],
                infoLinks: ['Membership', 'Purchase guide', 'Privacy policy', 'Terms of service'],
                socialIcons: [
                    {icon: 'fab fa-facebook-f'},
                    {icon: 'fab fa-twitter'},
                    {icon: 'fab fa-instagram'},
                    {icon: 'fab fa-linkedin-in'}
                ]
            };
        }
    };
</script>

<template>
    <footer class="footer">
        <div class="footer-container">
            <div class="footer-section">
                <h3>Address</h3>
                <p>{{ address }}</p>
                <p>{{ phone }}</p>
                <p><a>{{ email }}</a></p>
            </div>
            <div class="footer-section">
                <h3>Explore</h3>
                <ul>
                    <li v-for="(link, index) in exploreLinks" :key="index">{{ link }}</li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Information</h3>
                <ul>
                    <li v-for="(link, index) in infoLinks" :key="index">{{ link }}</li>
                </ul>
            </div>
            <div class="footer-section">
                <h3>Follow Us</h3>
                <div class="social-icons">
                    <a v-for="(social, index) in socialIcons" :key="index">
                        <i :class="social.icon"></i>
                    </a>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <p>© 2020 Maxcoach. All Rights Reserved</p>
        </div>
    </footer>
</template>

<style scoped>
    .footer {
        background-color: #333;
        color: white;
        padding: 30px 20px;
    }

    .footer-container {
        display: flex;
        justify-content: space-between;
        flex-wrap: wrap;
        gap: 20px;
    }

    .footer-section {
        flex: 1;
        min-width: 200px;
    }

    h3 {
        font-size: 18px;
        margin-bottom: 10px;
    }

    ul {
        list-style-type: none;
        padding: 0;
    }

    li {
        margin-bottom: 8px;
        cursor: pointer;
    }

    a {
        color: white;
        text-decoration: none;
    }

    a:hover {
        color: #20ad96;
    }

    .social-icons {
        display: flex;
        gap: 10px;
    }

    .social-icons a {
        color: white;
        font-size: 20px;
    }

    .footer-bottom {
        text-align: center;
        margin-top: 20px;
        font-size: 14px;
        border-top: 1px solid #444;
        padding-top: 10px;
    }
</style>
