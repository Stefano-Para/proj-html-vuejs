<template>
    <section id="circle-graphs">
        <div class="container-dimension container-circles3">
            <!-- first graph  -->
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
            <!-- second graph  -->
            <div class="background-green">
                <div class="container-circle">
                    <i class="far fa-circle fa-9x"></i>
                    <div class="white-circle">
                        <h2>100%</h2>
                    </div>
                        <h5>Pass Rate</h5>
                </div>
            </div>
            <!-- third graph  -->
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
</template>

<script>
export default {
    name: 'Graphs'
}
</script>

<style lang="scss" scoped>
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
</style>