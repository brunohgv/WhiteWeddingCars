<template>
  <b-container fluid class="vertical-space">
    <h3>White Wedding Cars</h3>
    <hr>
    <b-container class="container-space">
      <b-row align-self="center">
        <b-col cols="12" md="12">
          <b-img class="div-img" :src="require('../assets/LMT_3032.jpg')" fluid thumbnail alt=""/>
          <p>{{ texto1 }}</p>
          <p>{{ texto2 }}</p>
          <p>{{ texto3 }}</p>
        </b-col>
      </b-row>
      <b-row>
        <b-card-group class="margin-card" deck>
          <b-card header="Pacote Ouro"
                  class="text-center">
              <p class="card-text">Pega a noiva no hotel/salão de beleza, leva até a igreja e de lá leva os noivos até a casa de recepção.</p>
          </b-card>
          <b-card header="Pacote Diamante"
                  class="text-center">
              <p class="card-text">Pega a noiva no hotel/salão de beleza, leva até a igreja e de lá leva os noivos até a casa de recepção. Aguarda o final da festa e deixa os noivos no hotel.</p>
          </b-card>
        </b-card-group>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      texto1: 'A White Wedding Cars é uma empresa pernambucana especializada em aluguel de carros brancos para casamentos. A ideia surgiu quando seu idealizador identificou que os carros brancos estão cada vez mais sendo procurados pelos noivos para deixarem o seu dia “D” ainda mais especial. Se as noivas gostam de casar de branco por que não chegar no casamento num carro branco? Esse efeito, segundo fotógrafos e empresas de filmagem, fica espetacular.',
      texto2: 'Contamos com uma equipe experiente que preza pela qualidade e pontualidade do serviço prestado. Para atingir nosso objetivo temos duas opções de carros bem exclusivos, sendo um PT Cruiser, que é o único branco do Nordeste e um dos poucos brancos do Brasil, e um Ford Fusion, também branco, claro, adquirido recentemente para atender o público que prefere um carro mais clássico, uma vez que trata-se de um sedan de grande porte e extremamente confortável.  Nossos carros são muito bem conservados e você pode conhecê-los antes de contratar nosso serviço.',
      texto3: 'Entre em contato conosco para conhecer nossos pacotes, que oferecem, ambos, como cortesia, um Champanhe Chandon, juntamente com duas taças personalizadas, para o primeiro brinde do casal:'
    }
  }
}
</script>

<style scoped>
.vertical-space{
  min-height: 100vh;
  padding-top: 4em;
  background: #fff;
}
.container-space {
  margin-top: 2em;
}
h3 {
  font-family: 'Cormorant Garamond', serif;
  text-align: center;
  font-size: 72px
}
p{
  font-family: 'Raleway', sans-serif;
}
.div-img{
	float: left;
	max-width: 50%;
	margin-right: 15px;
	border-radius: 10px;
}
p {
  text-align: justify
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
@media (max-width: 768px) {
  .second-col {
    margin-top: 2em;
  }
  .div-img{
    float: none;
    max-width: 100%;
    margin-right: 0px;
    border-radius: 10px;
  }
}
.margin-card {
  margin-bottom: 2em;
}
</style>
