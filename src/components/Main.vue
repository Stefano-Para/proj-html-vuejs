<template>
    <main>
        
        <Signup />

        <Drivetoday />

        <Courses />

        <Graphs />

        <Istructors :istructors="istructors"/>
        
        <Slider />

        <Lastnews />

  </main>
</template>

<script>
import Slider from './Slider.vue'
import Istructors from './Istructors.vue'
import Graphs from './Graphs.vue'
import Courses from './Courses.vue'
import Drivetoday from './Drivetoday.vue'
import Signup from './Signup.vue'
import Lastnews from './Lastnews.vue'

export default {
    name: 'Main',
    components: {
        Slider,
        Istructors,
        Graphs,
        Courses,
        Drivetoday,
        Signup,
        Lastnews
    },
    props: {
        istructors: Array
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
</style>