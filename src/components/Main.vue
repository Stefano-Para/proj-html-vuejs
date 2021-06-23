<template>
    <main>
        <!-- section 1/5 registration white -->
        <section id="sign-up" >
        <div class="container-dimension">
            <div class="column-50">
                <h2>Get Behing The Wheel</h2>
                <h4>Lorem, ipsum dolor sit amet consectetur adipisicing elit. In quaerat iure quidem ex ratione adipisci dignissimos deserunt placeat.
                </h4>
                <p>Lorem ipsum dolor, sit amet consectetur adipisicing elit. Velit distinctio amet, quia veniam ad vitae molestiae aperiam! Tempora, rerum cumque. Enim atque, sunt tempore mollitia ab dolorum! Architecto, nam suscipit. Lorem ipsum dolor sit amet consectetur adipisicing elit. Error, amet! Lorem ipsum, dolor sit amet consectetur adipisicing elit. Eligendi, molestiae.</p>
            </div>
            <div class="column-50 column-absolute">

                    <div id="text-absolute">
                        <h2>First Lesson Free</h2>
                        <h4>When you make a block booking with us your first lesson is included free.</h4>
                    </div>

                    <form id="registration" action="/action_page.php">
                        <div id="container-input-img">
                            <input type="text" name="name" placeholder="Your Name*">
                            <a href=""><img src="../assets/image.png" alt=""></a>  
                        </div>
                        
                        <input type="email" name="email" placeholder="Email*">

                        <input type="number" placeholder="Telephone">

                        <input type="text" name="location" placeholder="Location">
                    </form>
                    <button>Request a Callback</button>

            </div>
        </div>
        </section>
        <!-- section 2/5 drive today + phone  -->
        <section id="drive-today">
            <div class="container-dimension">
                <div class="column-50">
                    <h2>Start Learning to Drive Today</h2>
                    <h5>Give us a call to schedule your first driving lesson</h5>
                </div>
                <div class="column-50">
                    <h4>
                        <i class="fas fa-phone"></i>
                        1-800-555-555
                    </h4>
                </div>
            </div>
        </section>
        <!-- section 3/5 instructor sect  -->
        <section id="instructorsNDcourses">

            <!-- absolute part top of section  -->
            <section id="courses-container">
                <!-- non posso metterla come background perchè mi da un errore di chrome non da console solita ma per privacy (errore giallo) -->
                <svg class="fusion-big-triangle-candy" xmlns="http://www.w3.org/2000/svg" version="1.1" width="100%" height="100" viewBox="0 0 100 100" preserveAspectRatio="none" style="fill:#e4eaed;padding:0;"><path d="M-1 -1 L50 99 L101 -1 Z"></path></svg>

                <div class="container-dimension">
                    <!-- 1 colonna -->
                    <div class="column4 column4-absolute">
                        <img src="../assets/new-corner.jpg" alt="">
                        <h2>Courses</h2>
                        <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Quia expedita voluptate qui veritatis iusto magni dolorum sapiente quas. Lorem ipsum dolor sit amet.</p>
                        <button>Course Information</button>
                    </div>
                    <!-- 3 colonne  -->
                    <div id="container-3column">
                        <div class="column4">
                        <img src="../assets/courses-passplus-200x200.jpg" alt="">
                        <h3>Pass Plus</h3> 
                        <button>Learn More</button>
                    </div>
                    <div class="column4">
                        <img src="../assets/course-intensive-200x200.jpg" alt="">
                        <h3>Pass Plus</h3> 
                        <button>Learn More</button>
                    </div>
                    <div class="column4">
                        <img src="../assets/courses-instructor-200x200.jpg" alt="">
                        <h3>Pass Plus</h3> 
                        <button>Learn More</button>
                    </div>
                    </div>
                </div>

            </section>
            <!-- second part with istructors & circle graphs -->
            <section>
                <div class="container-dimension container-circles3">
                    <div class="background-green">
                        <div class="container-circle">
                            <i class="fas fa-circle-notch fa-9x"></i>
                            <div class="white-circle">
                                <div class="green-circle-small"></div>
                                <h2>95%</h2>
                            </div>
                                <h5>Pass Rate</h5>
                        </div>
                    </div>
                    <div class="background-green">
                        <div class="container-circle">
                            <i class="far fa-circle fa-9x"></i>
                            <div class="white-circle">
                                <h2>100%</h2>
                            </div>
                                <h5>Pass Rate</h5>
                        </div>
                    </div>
                    <div class="background-green">
                        <div class="container-circle">
                            <div class="grey-circle">
                                <div class="green-circle-small"></div>
                            </div>
                            <div class="white-circle">
                                <h2>95%</h2>
                            </div>
                                <h5>Pass Rate</h5>
                        </div>
                    </div>
                </div>
            </section>
            <!-- thir part "your istructors" -->
            <section id="container-your-istructors">
                <div class="container-dimension">
                    <h2>Your Istructors</h2>
                    <div id="textNDbutton">
                        <p>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Iure, nostrum. Doloremque sint id eius accusamus esse. Facilis obcaecati omnis..</p>
                        <button>More about us</button>
                    </div>
                </div>
                <!-- import data from app building 3 cards  -->
                <div id="container-istructors-cards">
                    <div class="container-dimension">
                        <div v-for="(istructor, index) in istructors"
                        :key="index"
                        class="container-single-card">
                            <img :src="require(`../assets/${istructor.img}`)" alt="">
                            <h3>{{ istructor.name }}</h3>
                            <ul>
                                <li>
                                    <a href=""><i class="fab fa-facebook-f"></i></a>
                                    <a href=""><i class="fab fa-twitter"></i></a>
                                    <a href=""><i class="fab fa-instagram"></i></a>
                                </li>
                            </ul>
                            <p>Lorem, ipsum dolor sit amet consectetur adipisicing elit.</p>
                        </div>
                    </div>
                </div>
            </section>
            <!-- forth part with Testimonials bg-->
            <section id="testimonials">
                <!-- container all testimonials  -->
                <div class="container-dimension">
                    <h2>Testimonials</h2>
                    <p>Here's what our happy drivers had to say about our services:</p>
                    <!-- dinamic slider  -->
                    <div class="dinamic-testimonials">
                        <img src="../assets/testimonial-sophia.png" alt="">
                        <p>Avada Driving School really helped build my confidence behind the wheel and with driving in general, and they got me a first time pass! Hightly reccomended.</p>
                        <h5>Sophia Jones</h5>
                    </div>
                </div>

            </section>
        </section>

  </main>
</template>

<script>
export default {
    name: 'Main',
    props: {
        istructors: Array
    },
    methos: function() {

    }
}
</script>

<style lang="scss" scoped>
// FIRST SECTION 
#sign-up {
    background-color: white;
    height: 480px;
    color: #494c4e;
    .container-dimension {
        display: flex;
        justify-content: space-between;
        padding: 40px 0 20px;
        position: relative;
        // column left 
        .column-50 {
            width: 48%;
            padding: 20px 0;
            h2 {
                font-weight: 600;
            }
            h4 {
                font-weight: 400;
                margin: 20px 0;
                line-height: 1.6em;
                letter-spacing: 0.5px;
            }
            p {
                font-size: 12px;
                letter-spacing: 1px;
                line-height: 1.8em;
                font-weight: 300;
            }
        }
        // column right
        .column-absolute {
            box-shadow: 0px 3px 10px 3px rgba($color: #000000, $alpha: 0.1);
            background-color: white;
            border-radius: 7px;
            width: 45%;
            position: absolute;
            top: -25px;
            right: 0;
            padding: 25px;
            display: flex;
            flex-direction: column;
            #text-absolute {
                text-align: center;
                h2 {
                    color: #7ABC64;
                }
                h4 {
                    font-weight: 300;
                    font-size: 12px;
                    margin: 20px 0;
                    line-height: 1.5em;
                    letter-spacing: 0.5px;
                    color: #494c4e;
                }
            }
            #registration {
                display: flex;
                flex-direction: column;
                justify-content: space-between;
                align-items: stretch;
                padding: 10px;
                color: #494c4e;
                #container-input-img {
                    position: relative;
                    input {
                        width: 100%;
                    }
                    img {
                        width: 15px;
                        height: 17px;
                        position: absolute;
                        top: 22px;
                        right: 10px;
                    }
                }
                input {
                    font-size: 12px;
                    border-radius: 3px;
                    border: 1px solid #494c4e;
                    background-color: rgba(223, 217, 217, 0.301);
                    margin: 10px 0;
                    height: 40px;
                    padding: 0px 10px;
                }
            }
            button {
                text-transform: uppercase;
                font-size: 12px;
                color: white;
                width: 50%;
                margin: 10px auto;
                background-color: #7ABC64;
                padding: 7px 20px;
                border: white;
                border-radius: 12px;
                &:hover {
                    transform: scale(0.9)
                }
            }
        }
    }
}
// SECOND SECTION 
#drive-today {
    height: 190px;
    background-image: url(../assets/horizontal-cta-background.jpg);
    background-size: cover;
    background-position: center;
    color: white;
    .container-dimension {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 90%;
        padding: 15px 0;
        .column-50 {
            width: 48%;
            padding: 20px 0;
            h2 {
                font-size: 35px;
                font-weight: 600;
                margin-bottom: 5px;
            }
            h5 {
                font-size: 18px;
                font-weight: 500;
            }
            h4 {
                height: 25px;
                transform: scale(1.6);
                font-weight: 400;
                text-align: center;
                i {
                    margin: 10px;
                }
            }
        }
    }
}
// THIRD SECTION 
#instructorsNDcourses {
    // height: 900px;
    #courses-container {
        position: relative;
        height: 450px;
        background-image: url(../assets/promise-background.jpg);
        background-size: 100%;
        background-position: bottom;
        svg {
            position: absolute;
            width: 100%;
            bottom: -99px;
        }
        .container-dimension {
            display: flex;
            justify-content: space-between;
            text-align: center;
            padding: 50px 0;
            #container-3column {
                display: flex;
                justify-content: space-between;
                width: 60%;
            }
            .column4 {
                width: 30%;
                display: flex;
                flex-direction: column;
                color: #7799ad;
                padding: 10px;
                h3 {
                    font-weight: 500;
                    margin: 5px 0;
                }
                button {
                    text-transform: uppercase;
                    font-weight: 500;
                    color: #7799ad;
                    margin: 5px auto;
                    padding: 5px 20px;
                    border: 3px solid;
                    border-radius: 15px;
                    &:hover {
                        color: #7ABC64;
                    }
                }
                
            }
            .column4-absolute {
                width: 34%;
                position: relative;
                box-shadow: 0px 20px 20px 10px rgba($color: #000000, $alpha: 0.1);
                top: -80px;
                background-color: white;
                border-radius: 10px;
                padding: 15px;
                img {
                    position: absolute;
                    width: 50px;
                    left: 0;
                    top: 0;
                    overflow: hidden;
                    border-radius: 2px;
                }
                h2 {
                    margin: 10px 0;
                }
                p {
                    line-height: 30px;
                    margin: 20px 0 30px;
                }
                button {
                    text-transform: uppercase;
                    color: white;
                    background-color: #7ABC64;
                    border: 0;
                    margin: 20px auto 30px;
                    padding: 7px 20px;
                    &:hover {
                        transform: scale(0.9);
                    }
                }
            }
        }
    }
    .container-circles3 {
        display: flex;
        height: 150px;
        justify-content: space-between;
        position: relative;
        color: #7799ad;
        text-transform: uppercase;
        .background-green {
            box-shadow: 
                0px 16px 15px 5px rgb(0 0 0 / 10%),
                0px 0px #7ABC64;
            background-color: #7ABC64;
            height: 360px;
            width: 32.5%;
            border-radius: 10px;
            .container-circle {
                background-color: white;
                width: 100%;
                height: 360px;
                top: 7px;
                border-radius: 10px;
                display: flex;
                flex-direction: column;
                justify-content: center;
                align-items: center;
                position: relative;
                i {
                    font-size: 220px;
                    color: #7ABC64;
                    transform: rotate(-10deg)
                }
                h5 {
                    width: 100%;
                    text-align: center;
                    margin: 10px auto 0;
                    font-weight: 500;
                }
                .grey-circle {
                    position: relative;
                    z-index: 1;
                    height: 215px;
                    width: 215px;
                    border-radius: 50%;
                    background-color: #eeeeee;
                }
                .white-circle {
                    position: absolute;
                    background-color: white;
                    z-index: 1;
                    bottom: 97px;
                    height: 192px;
                    width: 192px;
                    border-radius: 50%;
                    h2 {
                        font-size: 40px;
                        position: absolute;
                        z-index: 1;
                        top: 50%;
                        left: 50%;
                        transform: translate(-45%, -50%);
                    }
                }
                .green-circle-small:last-child {
                    position: relative;
                    left: 50%;
                    transform: translate(-50%);
                    z-index: 1;
                    border-radius: 50%;
                    background-color: #7ABC64;
                    height: 12px;
                    width: 12px;
                }
            }
        }
    }
    #container-your-istructors {
        margin-top: 300px;
        #textNDbutton {
            display: flex;
            justify-content: space-between;
            align-items: flex-end;
            margin: 20px 0;
            p {
                margin-top: 10px;
                width: 60%;
                letter-spacing: 0.5px;
                line-height: 25px;
                color: #7799ad;
            }
            button {
                text-transform: uppercase;
                font-weight: bold;
                color: white;
                padding: 10px 70px;
                background-color: #7ABC64;
                border-radius: 20px;
                border: 0;
                &:hover {
                    transform: scale(0.8);
                }
            }
        }
        #container-istructors-cards {
            height: 370px;
            .container-dimension {
                display: flex;
                justify-content: space-between;
                text-align: center;
                padding: 30px 0;
                .container-single-card {
                    box-shadow: 
                        0px 16px 15px 5px rgb(0 0 0 / 10%),
                        0px -6px #7ABC64;
                    background-color: white;
                    color: #bebdbd;
                    border-radius: 10px;
                    height: 400px;
                    width: 34%;
                    padding: 15px;
                    &:first-child,
                    &:last-child {
                        width: 32%;
                        height: 390px;
                    }
                    img {
                        width: 250px;
                    }
                    h3 {
                        color: #494c4e;
                        margin: 20px 0 10px;
                        font-size: 25px;
                        font-weight: 600;
                    }
                    ul {
                        list-style-type: none;
                        a {
                            margin: 10px;
                            text-decoration: none;
                            color: #bebdbd;;
                        }
                    }
                    p {
                        font-size: 14px;
                        padding: 0px 15px;
                        letter-spacing: 0.5px;
                        line-height: 25px;
                    }
                }
            }
        }
    }
}
#testimonials {
    background-image: url('../assets/testimonial-background.jpg');
    background-size: cover;
    background-position: center;
    height: 700px;
    .container-dimension {
        height: 100%;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        color: #95a5b2;
        h2 {
            color: #494c4e;
            font-weight: 600;
            font-size: 30px;
        }
        p {
            font-size: 18px;
            font-weight: 400;
        }
        .dinamic-testimonials {
            text-align: center;
            img {
                width: 15%;
                margin: 40px;
            }
            p {
                font-size: 16px;
                width: 50%;
                margin: 0 auto;
                line-height: 25px;
                font-weight: 400;
            }
        }
    }
}

</style>