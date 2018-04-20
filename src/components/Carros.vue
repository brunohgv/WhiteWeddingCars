<template>
  <b-container fluid class="vertical-space">
    <!-- <img class="background" :src="foto3" alt=""> -->
    <h3>Nossos Carros</h3>
    <hr>
    <b-container class="container-space">
      <b-row align-self="center">
        <b-col class="margincol text-center" cols="12" md="6">
          <!-- <div class="effect">
            <b-img class="image" :src="require('../assets/LMT_2999.jpg')" fluid alt=""/>
            <div class="middle">
              <div class="text">Chrysler PTCruiser TRG</div>
            </div>
          </div> -->
          <b-card img-src="../assets/LMT_2999.jpg"
                img-alt="Card image"
                img-top
                title="Chrysler PTCruiser">
            <!-- <p class="card-text">
                Chrysler PTCruiser TRG
            </p> -->
            <b-btn variant="outline-dark" class="btn-center" v-b-modal.modal1>Saiba mais</b-btn>
          </b-card>
          <!-- modal -->
          <b-modal
              id="modal1"
              size="lg"
              title="Chrysler PTCruiser"
              ok-only
              ok-variant="secondary">
            <b-img :src="require('../assets/LMT_3032.jpg')" fluid></b-img>
            <p class="my-4">{{ ptcruiserText }}</p>
          </b-modal>
        </b-col>
        <b-col class="margincol margin text-center" cols="12" md="6">
          <!-- <div class="effect">
            <b-img class="image" :src="require('../assets/SAL_4921.jpg')" fluid alt=""/>
            <div class="middle">
              <div class="text">Ford Fusion</div>
            </div>
          </div> -->
          <b-card img-src="../assets/SAL_4921.jpg"
                img-alt="Card image"
                img-top
                title="Ford Fusion">
            <!-- <p class="card-text">
                Ford Fusion
            </p> -->
            <b-btn variant="outline-dark" class="btn-center" v-b-modal.modal2>Saiba mais</b-btn>
          </b-card>
          <!-- modal -->
          <b-modal
              id="modal2"
              size="lg"
              title="Ford Fusion"
              ok-only
              ok-variant="secondary">
            <b-img :src="require('../assets/SAL_5082.jpg')" fluid></b-img>
            <p class="my-4">{{ fusionText }}</p>
          </b-modal>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
import LMT_2999 from '@/assets/LMT_2999.jpg'
import SAL_4921 from '@/assets/SAL_4921.jpg'
import SAL_5071 from '@/assets/SAL_5071.jpg'
export default {
  data () {
    return {
      foto1: LMT_2999,
      foto2: SAL_4921,
      foto3: SAL_5071,
      ptcruiserText: 'O PT Cruiser é um carro americano, produzido pela Chrysler. Conhecido como um carro de estilo “retrô”, esse modelo é um dos preferidos pelas noivas pelo seu design super arrojado. Nosso exemplar é muitíssimo pouco rodado, uma vez que é utilizado apenas em pequenos passeios e para transportar os noivos no dia mais importante de suas vidas. Além de muito novo, ele possui um teto solar que dá a ele um charme ainda maior. Vale à pena lembrar que ele é o único PT Cruiser Branco do Nordeste. Mais exclusivo que usar este carro no dia do seu casamento é praticamente impossível.',
      fusionText: 'Para quem prefere um estilo mais clássico temos, como opção, um Ford Fusion, branco também, é claro. É um sedã de grande porte e extremamente confortável, além de muito conservado. O carro chama a atenção por onde passa, uma vez que, assim como o PT Cruiser, o Fusion branco não é muito fácil de encontrar no mercado. Além de muito espaçoso ele é realmente extremamente bonito e glamouroso. Você chegará em grande estilo no seu casamento.'
    }
  }
}
</script>

<style scoped>
.vertical-space{
  min-height: 100vh;
  padding-top: 4em;
  position: relative;
  background: #fff;
}
.image {
  border-radius: 5px;
}
.effect .image{
  filter: brightness(1);
  transition: ease-in-out 0.5s;
}
.effect:hover .image{
  filter: brightness(0.2);
  transition: ease-in-out 0.5s;
}
.middle {
  transition: .5s ease;
  opacity: 0;
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  -ms-transform: translate(-50%, -50%);
  text-align: center;
}
.effect:hover .middle{
  opacity: 1;
  transition: ease-in-out 0.5s;
}
.text {
  color: white;
}
.background {
  position: absolute;
  top: 0%;
  left: 0%;
  width: 100%;
  height: 100%;
  z-index: -1;
  filter: brightness(0.1) sepia(1);
  object-fit: cover;
}
.btn-center {
  margin-top: 1em;
}
.margincol {
  margin-top: 1em;
}
.margin {
  margin-bottom: 3em; 
}
p {
  text-align: justify
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
