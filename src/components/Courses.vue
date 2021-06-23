<template>
    <section id="courses-container">
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
</template>

<script>
export default {
    name: 'Courses'
}
</script>

<style lang="scss" scoped>
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
</style>