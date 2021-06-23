<template>
    <section id="testimonials">
        
        <!-- <div class="container-dimension">
            <h2>Testimonials</h2>
            <p>Here's what our happy drivers had to say about our services:</p>
            <div class="dinamic-testimonials">
                <img src="../assets/testimonial-sophia.png" alt="">
                <p>Avada Driving School really helped build my confidence behind the wheel and with driving in general, and they got me a first time pass! Hightly reccomended.</p>
                <h5>Sophia Jones</h5>
            </div>
        </div> -->

        <div
        
         class="container-dimension">
            <h2>Testimonials</h2>
            <p>Here's what our happy drivers had to say about our services:</p>
            <!-- dinamic slider  -->
            <div class="dinamic-testimonials">
                <img
                :src="testimonials[imageIndex].img"
                alt="">
                <p>
                    {{ testimonials[imageIndex].text }}
                </p>
                <h5>{{ testimonials[imageIndex].name }}</h5>
                <!-- how to slide  -->
                <div class="fixed-dots">
                    <i
                    v-for="(testimonial, index) in testimonials"
                    :key="index"
                    class="far dot fa-circle"
                    :class="(index == imageIndex) ? 'fas' : 'far'"
                    @click="imageIndex = index"
                    ></i>
                </div>
            </div>
        </div>
    
    </section>
</template>

<script>

export default {
    name: 'Slider',
    data: function() {
        return {
            imageIndex: 0,
            testimonials: [
                {
                    name: 'Sophia jones',
                    img: require('../assets/testimonial-sophia.png'),
                    text: 'Avada Driving School really helped build my confidence behind the wheel and with driving in general, and they got me a first time pass! Hightly reccomended.'
                },
                {
                    name: 'Grant Fantastichair',
                    img: require('../assets/testimonial-grant.png'),
                    text: 'Ehi i dunno what ima doing about driving but "ehi": look at my hairs'
                },
                {
                    name: 'Kate Larossa',
                    img: require('../assets/testimonial-kate.png'),
                    text: 'Im so happy about this site, so to celebrate this built i have decided to change my hair color into red '
                },
                {
                    name: 'Kelly Lelly',
                    img: require('../assets/testimonial-kelly.png'),
                    text: 'I\'ve sent my curriculum at models Accademy but i got contacted by theese guys. Not the best job but neither the worst'
                },
                {
                    name: 'Harold The Beautiful',
                    img: require('../assets/testimonial-harold.png'),
                    text: 'Yes. Im not the best superman ever seen, but im the superman that everybody needs.'
                }
            ],
        }
    }
    }

</script>

<style lang="scss" scoped>
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
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: space-between;
            height: 300px;
            position: relative;
            img {
                width: 200px;
                height: 200px;
                margin: 20px;
            }
            p {
                font-size: 16px;
                width: 50%;
                margin: 0 auto;
                line-height: 25px;
                font-weight: 400;
            }
            h5 {
                margin: 10px 0 20px;
            }
            .fixed-dots {
                position: absolute;
                bottom: -80px;
            }
        }
    }
}

</style>