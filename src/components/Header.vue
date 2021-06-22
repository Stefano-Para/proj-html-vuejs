<template>
  <header>

      <section id="top-header">
          <div class="container-dimension">
              <h5>
                  We have a 95% Successful Pass Rate!
              </h5>

              <h5>
                  <i class="fas fa-phone"></i>
                  Give us a call to book your tuition! 1-800-555-555
              </h5>
          </div> 
      </section> 

      <!-- jumbotron + navbar  -->
      <section id="mid-header">

          <div id="jumbotron">
              <div class="container-text container-dimension">
                    <h1>Drive with Avada</h1>
                    <p>We offer the finest driving tuition money can buy</p>
              </div>
          </div>
          <!-- navbar  -->
          <div id="navbar">
              <div class="container-dimension">
                    <a href="">
                        <img src="../assets/avada-drivers-logo-1x.png" alt="">
                    </a>
                    <ul >
                        <li v-for="(item, i) in navbar"
                        :key="i"
                        @click="setActive(item.link)"
                        :class="{active : active_index == item.link}"
                        >
                            {{ item.link }}
                            <div v-if="item.class == 'new' ">
                                <button>new</button>
                            </div>
                        </li>
                    </ul>
                    
              </div>
          </div>

      </section>
  </header>
</template>

<script> 

export default {
    name: 'Header',
    data: function() {
        return {
            navbar: [
                {
                    link: 'home',
                    status: 'active'
                },
                {
                    link: 'about',
                    status: 'inactive'
                },
                {
                    link: 'prices',
                    status: 'inactive'
                },
                {
                    link: 'courses',            
                    status: 'inactive',
                    class: 'new',
                    
                },
                {
                    link: 'location',
                    status: 'inactive'
                },
                {
                    link: 'blog',
                    status: 'inactive'
                },
                {
                    link: 'bookNow',
                    status: 'inactive'
                },
            ],
            active_index: 0,
        }
    },
    methods:{
        setActive: function(clicked) {
            this.active_index = clicked;
        }
    },
    mounted() {
      this.$nextTick(function(){
        window.addEventListener("scroll", function(){
          var navbar = document.getElementById("navbar")
          var nav_classes = navbar.classList
          if(document.documentElement.scrollTop >= 5) {
            if (nav_classes.contains("shrink") === false) {
              nav_classes.toggle("shrink");
            }
          }
          else {
            if (nav_classes.contains("shrink") === true) {
              nav_classes.toggle("shrink");
            }
          }
        })
      })
    },
}
</script>

<style lang="scss" scoped>

header {
    margin: 0 auto;
    #top-header {
        background-color: #333435;
        height: 40px;
        .container-dimension {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 100%;
            h5 {
                color: lightgrey;
                opacity: 0.4;
                font-size: 0.7em;
                i {
                    margin-right: 10px;
                }
            }
        }
    }
    #mid-header {
        #jumbotron {
            width: 100%;
            height: 500px;
            background-image: url(../assets/homepage-hero-background.jpg);
            background-size: cover;
            color: white;
            position: relative;
            .container-text {
                position: relative;
                top: 50%;
                h1 {
                    font-weight: 600;
                    font-size: 2.5em;
                    padding: 10px 0;
                    letter-spacing: 1px;
                }
                p {
                    font-size: 1.05em;
                    font-weight: 300;
                }
            }
        }
        #navbar {
            height: 80px;
            width: 100%;
            color: white;
            position: fixed;
            top: 40px;
            background-color: rgba(90, 4, 4, 0.3);
            transition: all 0.2s;
            z-index: 2;
            &.shrink {
                top: 0;
                background-color: rgba(90, 4, 4, 0.6);
                }
            .container-dimension {
                display: flex;
                align-items: center;
                justify-content: space-between;
                height: 100%;
                a {
                    height: 100%;
                    display: flex;
                    align-items: center;
                    img {
                    height: 40%;
                }
            }
                ul {
                    display: flex;
                    align-items: center;
                    flex-grow: 1;
                    justify-content: space-between;
                    list-style: none;
                    margin-left: 200px;
                    li {
                        display: flex;
                        align-items: center;
                        font-size: 0.8em;
                        text-transform: uppercase;
                        text-decoration: none;
                        color: white;
                        &:hover,
                        &.active {
                            cursor: pointer;
                            padding: 5px 0;
                            border-bottom: 3px solid #7ABC64;
                            color: #7ABC64;
                            &:last-child {
                                color: white;
                            }
                        }
                        &:last-child {
                                padding: 7px 10px;
                                border-radius: 12px;
                                background-color: #7ABC64;
                                &:hover {
                                    transform: scale(0.8)
                                }
                        }
                        button {
                            color: white;
                            text-transform: uppercase;
                            font-size: 0.7em;
                            background-color: #7ABC64;
                            margin-left: 3px;
                            padding: 2px;
                            border: 0;
                            border-radius: 5px;
                            
                        }
                    }
                }
            }
        }
    }
}
</style>