<template>
  <section id="lastnews-container">
      <div class="container-dimension">

        <div class="lastnews">
            <h2>Lastest News</h2>
            <div class="container-columns">
                <div class="column left-column">
                    <img src="" alt="">
                rossa
                </div>
                <div class="column right-column">
                    interno macchina
                </div>
            </div>
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
    height: 650px;
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
            height: 500px;
            padding: 30px 0;
            h2 {
                text-align: center;
            }
            .container-columns {
                display: flex;
                justify-content: space-between;
                padding: 40px 0 20px;
                .column {
                    width: 50%;
                    text-align: center;
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