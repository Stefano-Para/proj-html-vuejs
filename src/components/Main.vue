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
                        <input type="text" name="name" placeholder="Your Name*">
                        
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

            <!-- second part of the section with istructors  -->
            <section>
                <div class="container-dimension container-circles3">
                    <div class="background-green">
                        <div class="container-circle">
                            <i class="fas fa-circle-notch fa-9x"></i>
                            <div class="white-circle">
                                <h2>95%</h2>
                            </div>
                                <h5>Pass Rate</h5>
                        </div>
                    </div>
                    <div class="background-green">
                        <div class="container-circle">
                            referral rate
                        </div>
                    </div>
                    <div class="background-green">
                        <div class="container-circle">
                            accidental rate
                        </div>
                    </div>
                </div>
            </section>
        </section>

  </main>
</template>

<script>
export default {
    name: 'Main'
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
    height: 900px;
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
            box-shadow: 0px 16px 15px 5px rgb(0 0 0 / 10%);
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
                }
                h5 {
                    width: 100%;
                    text-align: center;
                    margin: 10px auto 0;
                    font-weight: 500;
                }
                .white-circle {
                    position: absolute;
                    background-color: white;
                    bottom: 95px;
                    height: 198px;
                    width: 198px;
                    border-radius: 50%;
                    h2 {
                        font-size: 30px;
                        position: absolute;
                        top: 50%;
                        left: 50%;
                        transform: translate(-50%, -50%);
                    }
                }
            }
        }
    }
}

</style>