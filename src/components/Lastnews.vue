<template>
  <section id="lastnews-container">
      <div class="container-dimension">

        <div class="lastnews">
            <h2>Lastest News</h2>
            <div class="container-columns">
                <div class="column left-column">
                    <div class="container-img">
                        <img src="../assets/blog-choosecar-700x441.jpg" alt="">
                    </div>                    
                    <h4>What Car to Start With?</h4>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing</p>
                </div>
                <div class="column right-column">
                    <div class="container-img">
                        <img src="../assets/blogpost-10and2-700x441.jpg" alt="">
                    </div>
                    <h4>Avada Driving School Expanding</h4>
                    <p>Lorem ipsum dolor, sit amet consectetur adipisicing</p>
                </div>
            </div>
            <button>More from the blog</button>
        </div>

        <div class="triangle-bottom">
            <img src="../assets/latestnews-bottom.png" alt="">
        </div>

      </div>
  </section>
</template>

<script>
export default {
    name: 'Lastnews'
}
</script>

<style lang="scss" scoped>
#lastnews-container {
    height: 700px;
    background-image: url('../assets/latestnews-background.jpg');
    background-position: center;
    background-size: cover;
    position: relative;
    .container-dimension {
        position: absolute;
        left: 50%;
        top: -30px;
        transform: translate(-50%);
        box-shadow: 0px -7px #7ABC64;
        border-radius: 5px;
        .lastnews {
            border-radius: 5px;
            background-color: white;
            padding: 30px 0;
            h2 {
                text-align: center;
            }
            .container-columns {
                display: flex;
                justify-content: space-between;
                padding: 40px;
                position: relative;
                .column {
                    width: 48%;
                    text-align: center;
                    .container-img {
                        display: inline-block;
                        overflow: hidden; 
                        width: 100%;
                        height: 290px;
                        &:hover img {
                            transform: scale(1.1);
                            transform-origin: 50% 50%;
                        }
                        img {
                        width: 100%;
                        display: block;
                        transition: transform .8s;
                        }
                    }
                    h4 {
                        color: #7ABC64;
                        font-weight: 600;
                        margin: 10px 0;
                    }
                    p {
                        color: #929aa3;
                        font-size: 14px;
                    }
                }
            }
            button {
                display: block;
                margin: 0 auto;
                text-transform: uppercase;
                color: white;
                background-color: #7ABC64;
                padding: 5px 25px;
                border-radius: 20px;
                border: 0;
                &:hover {
                    transform: scale(0.9);
                }
            }
        }
        .triangle-bottom {
            img {
                position: relative;
                top: -0.5px;
                width: 100%;
            }
        }
    }
}
</style>