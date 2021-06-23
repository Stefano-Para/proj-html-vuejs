<template>
  <div id="app">

    <Header />

    <Main :istructors="istructors" />

    <Footer />

  </div>
</template>

<script>
import Header from './components/Header.vue'
import Footer from './components/Footer.vue'
import Main from './components/Main.vue'

export default {
  name: 'App',
  components: {
    Header,
    Footer,
    Main
  },
  data: function() {
    return {
      istructors: [
        {
          name: 'Mike Hart',
          img: 'instructor-mikehart-400x254.jpg',
          text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
        },
        {
          name: 'John Smith',
          img: 'instructor-johnsmith-400x254.jpg',
          text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
        },
        {
          name: 'Angela Hart',
          img: 'instructor-angelahart-400x254.jpg',
          text: 'Lorem, ipsum dolor sit amet consectetur adipisicing elit.'
        },
      ]
    }
  }
}
</script>

<style lang="scss">
@import '~@fortawesome/fontawesome-free/css/all.min.css';

* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
.container-dimension {
    width: 70%;
    margin: 0 auto;
}
button:hover {
  cursor: pointer;
}
</style>
