<template>
    <footer>

        <section id="footer-top">
            <div class="container-dimension">
                    <!-- 1/4 logo + text -->
                    <section>
                        <img src="../assets/avada-drivers-logo-1x.png" alt="">
                        <p>Avada Driving School is the right choice for experienced drivers looking for a refresher course, or the brand new driver wanting to pass first time.</p>
                    </section>
                    <!-- 2/4 contacts -->
                    <section>
                        <h2>Contact details</h2>
                        <ul>
                            <li
                            v-for="(item, index) in footerContacts"
                            :key="index"
                            >
                            <i
                            :class="item.icon"></i>
                            {{ item.text }}
                            </li>
                        </ul>
                    </section>
                    <!-- 3/4 courses -->
                    <section>
                        <h2>Courses</h2>
                        <ul>
                            <li
                            v-for="(item, index) in coursesList"
                            :key="index"
                            >
                                <a href="">
                                    <i class="fas fa-arrow-circle-right green"></i>
                                    {{ item.text }}
                                </a>
                            </li>
                        </ul>
                    </section>
                    <!-- 4/4 img + button -->
                    <section>
                        <img src="../assets/footer-ad-grid.png" alt="">
                        <a href="">
                            <button>
                                Book Now
                            </button>
                        </a>
                    </section>
            </div>
        </section>

        <section id="footer-bottom">
            <div class="container-dimension">
                <h6>
                    © Copyright 2021 - 2020 | Avada Theme by <span>ThemeFusion</span> | All right Reserved | Powered by <span>WordPress</span>
                </h6>
                <ul>
                    <li v-for="(item, i) in socials"
                    :key="i">
                        <a :href="item.url">
                            <i :class="item.socialIcon"></i>
                        </a>
                    </li>
                </ul>
            </div>
        </section>

    </footer>
</template>

<script>
export default {
    name: 'Footer',
    data: function() {
        return {
            footerContacts: [
                {
                        icon: "fas fa-home",
                        text: '12345 North Main Street, New York, NY 555555',
                    },
                    {
                        icon: 'fas fa-phone',
                        text: '1.800.555.6789'
                    },
                    {
                        icon: 'far fa-envelope',
                        text: 'info@your-domain.com'
                    },
                    {
                        icon: 'fas fa-link',
                        text: 'Theme-Fusion.com'
            }
            ],
            coursesList: [
                {
                text: 'Pass Plus'
                },
                {
                text: 'Intensive Course'
                },
                {
                text: 'Automatic'
                },
                {
                text: 'Istructor Training'
                },
            ],
            socials: [
                {
                    name:'facebook',
                    socialIcon: 'fab fa-facebook-f',
                    url: 'https://www.facebook.com/groups/AvadaUsers/'
                },
                {
                    name:'twitter',
                    socialIcon: 'fab fa-twitter',
                    url: 'https://twitter.com/theme_fusion'
                },
                {
                    name:'youtube',
                    socialIcon: 'fab fa-youtube',
                    url: 'https://www.youtube.com/results?search_query=avada'
                },
                {
                    name:'instagram',
                    socialIcon: 'fab fa-instagram',
                    url: 'https://www.instagram.com/themefusion/'
                }
            ]
        }
    }
}
</script>

<style lang="scss" scoped>
#footer-top {
    background-image: url(../assets/footer-background-color.jpg);
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 20px 0;
    .container-dimension {
            display: flex;
            justify-content: space-between;
            section {
                width: 25%;
                padding: 25px 10px;
                h2 {
                    text-transform: uppercase;
                    font-size: 0.9em;
                    color: white;
                    margin: 5px 0;
                }
                p {
                    margin-top: 10px;
                    font-size: 0.8em;
                    color: grey;
                }
                img {
                    margin-top: 5px;
                    width: 90%;
                }
                ul {
                    display: flex;
                    flex-direction: column;
                    list-style: none;
                    li {
                        color: grey;
                        font-size: 10px;
                        font-weight: 400;
                        margin: 5px 0;
                        i {
                            width: 20px;
                            height: 20px;
                            color: lightgrey;
                            &.green {
                                color: #7ABC64;
                            }
                        }
                        a {
                            color: #7ABC64;
                            text-decoration: none;
                            font-size: 12px;
                            &:hover {
                                opacity: 0.8;
                            }
                        }

                    }
                }
                button {
                    text-transform: uppercase;
                    color: white;
                    border: 0;
                    padding: 7px 10px;
                    border-radius: 12px;
                    background-color: #7ABC64;
                    margin: 20px 0;
                    &:hover {
                        transform: scale(0.8)
                    }
                }
                &:last-child {
                    display: flex;
                    flex-direction: column;
                    justify-content: center;
                    align-items: center;
                }
            }
    }
}
#footer-bottom {
    height: 80px;
    background-color: #1c1d1e;
    .container-dimension {
        height: 100%;
        display: flex;
        justify-content: space-between;
        align-items: center;
        h6 {
            font-size: 10px;
            font-weight: 400;
            color: grey;
            span {
                color: #7ABC64;
            }
        }
        ul {
            display: flex;
            list-style-type: none;
            li {
                font-size: 12px;
                a {
                    text-decoration: none;
                    color: white;
                    margin: 0 10px;
                    &:hover {
                        opacity: 0.5;
                    }
                }
            }
        }
    }
}
</style>