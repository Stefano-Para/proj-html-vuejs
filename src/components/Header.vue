<template>
  <header>

      <section id="top-header">
          <div class="container-70">
              <h5>
                  We have a 95% Successful Pass Rate!
              </h5>

              <h5>
                  <i></i>
                  Give us a call to book your tuition! 1-800-555-555
              </h5>
          </div> 
      </section> 

      <!-- jumbotron + navbar  -->
      <section id="mid-header">

          <div id="jumbotron">

          </div>
          <div id="navbar">

          </div>

      </section>
  </header>
</template>

<script>
export default {
    name: 'Header',

}
</script>

<style lang="scss" scoped>
.container-70 {
    width: 70%;
    margin: 0 auto;
}
header {
    margin: 0 auto;
    #top-header {
        background-color: #333435;
        height: 40px;
        .container-70 {
            display: flex;
            align-items: center;
            justify-content: space-between;
            height: 100%;
            h5 {
                color: lightgrey;
                opacity: 0.4;
                font-size: 0.7em;
            }

        }
    }
    #mid-header {
        #jumbotron {
            width: 100%;
            height: 500px;
            background-image: url(../assets/homepage-hero-background.jpg);
            background-size: cover;
        }
    }
}
</style>