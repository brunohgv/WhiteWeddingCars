<template>
  <b-container fluid class="vertical-space">
    <h3>{{ pagetitle }}</h3>
    <hr>
    <b-container class="space-container">
      <b-row>
        <b-col v-for="image in images" :key="image.link" lg="4" md="6" xs="6">
          <b-card img-fluid
                  overlay
                  :img-src="image.link"
                  class="hover-effect space"
                  @click="image.show = !image.show"></b-card>
          <b-modal v-model="image.show"
                size="lg"
                ok-only
                ok-variant="secondary">
            <b-img :src="image.link" fluid></b-img>
          </b-modal>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      pagetitle: 'Galeria de Fotos',
      images: [
        {link: require('../assets/LMT_0149.jpg'), id: 'modal1', show: false},
        {link: require('../assets/LMT_2999.jpg'), id: 'modal2', show: false},
        {link: require('../assets/SAL_4921.jpg'), id: 'modal3', show: false},
        {link: require('../assets/SAL_5071.jpg'), id: 'modal4', show: false},
        {link: require('../assets/LMT_3037.jpg'), id: 'modal5', show: false},
        {link: require('../assets/SAL_4957.jpg'), id: 'modal6', show: false},
        {link: require('../assets/SAL_5046.jpg'), id: 'modal7', show: false},
        {link: require('../assets/LMT_3032.jpg'), id: 'modal8', show: false},
        {link: require('../assets/SAL_5082.jpg'), id: 'modal9', show: false}
      ]
    }
  }
}
</script>

<style scoped>
.vertical-space {
  min-height: 100vh;
  padding-top: 4em;
  position: relative;
  background: #fff;
}
.hover-effect {
  opacity: 1;
  transition: ease-in-out 0.2s;
}
.hover-effect:hover {
  opacity: 0.8;
  cursor: pointer;
  transition: ease-in-out 0.2s;
}
.space {
  margin-bottom: 1em;
}
.space-container {
  margin-top: 2em;
  margin-bottom: 3em;
}
.margin-col {
  margin-left: 0.5em;
  margin-right: 0.5em;
}
h3 {
  font-family: 'Cormorant Garamond', serif;
  text-align: center;
  font-size: 72px
}
p{
  font-family: 'Raleway', sans-serif;
}
@media (max-width: 960px) {
  h3 {
    font-size: 48px
  }
  h1 {
    font-size: 72px
  }
}
@media (max-width: 720px) {
  h3 {
    font-size: 40px
  }
  h1 {
    font-size: 62px
  }
}
@media (max-width: 540px) {
  h3 {
    font-size: 32px
  }
  h1 {
    font-size: 44px
  }
}
</style>
