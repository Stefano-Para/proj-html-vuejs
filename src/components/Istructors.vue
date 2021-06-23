<template>
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
</template>

<script>
export default {
    name: 'Istructors',
    props: {
        istructors: Array
        }
}
</script>

<style lang="scss" scoped>
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
                    transition: transform .6s; 
                    &:hover {
                        transform: scale(1.03);
                        box-shadow: 
                            0px 10px 10px rgb(0 0 0 / 10%)
                    }
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
</style>