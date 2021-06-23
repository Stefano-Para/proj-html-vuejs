<template>
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
</template>

<script>
export default {
    name: 'Drivetoday'
}
</script>

<style lang="scss" scoped>
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
</style>