<template>
  <b-container fluid class="vertical-space">
    <h3>{{ pagetitle }}</h3>
    <hr>
    <b-container class="space-container">
      <b-row>
        <b-col md="12" lg="6" class="margin">
          <b-form method="POST" action="https://formspree.io/contato@whiteweddingcars.com.br">
            <b-form-group id="exampleInputGroup1"
                        label="Nome:"
                        label-for="exampleInput1">
            <b-form-input id="exampleInput1"
                          type="text"
                          name="Nome"
                          required
                          placeholder="Digite seu nome">
            </b-form-input>
            </b-form-group>
            <b-form-group id="exampleInputGroup2"
                        label="Email:"
                        label-for="exampleInput2">
            <b-form-input id="exampleInput2"
                          type="email"
                          name="Email"
                          required
                          placeholder="Insira seu email">
            </b-form-input>
            </b-form-group>
            <b-form-group id="exampleInputGroup3"
                        label="Telefone:"
                        label-for="exampleInput3">
            <b-form-input id="exampleInput3"
                          name="Telefone"
                          required
                          placeholder="Insira seu telefone">
            </b-form-input>
            </b-form-group>
            <b-form-group id="exampleInputGroup4"
                        label="Assunto:"
                        label-for="exampleInput4">
            <b-form-input id="exampleInput4"
                          name="Assunto"
                          required
                          placeholder="Insira o assunto">
            </b-form-input>
            </b-form-group>
            <b-form-group id="exampleInputGroup5"
                        label="Mensagem:"
                        label-for="exampleInput5">
            <b-form-textarea id="exampleInput5"
                          name="Mensagem"
                          v-model="message"
                          required
                          :rows="4"
                          placeholder="Mensagem">
            </b-form-textarea>
            <input type="hidden" name="_next" value="whiteweddingcars.com.br" />
            </b-form-group>
            <b-button type="submit" variant="outline-dark">Enviar</b-button>
          </b-form>
        </b-col>
        <b-col md="12" lg="6" class="margin">
          <div class="custom-contact">
            <h4>{{ contactMessage }}</h4>
            <p v-for="option in contactOptions" :key="option.name"><i :class="option.icon"></i> {{option.content}}</p>
          </div>
          <div class="custom-contact">
            <a v-for="media in social" :key="media.icon" :href="media.link" target="_blank"><i :class="media.icon"></i></a>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </b-container>
</template>

<script>
export default {
  data () {
    return {
      pagetitle: 'Contato',
      contactMessage: 'Ou entre em contato conosco por',
      contactOptions: [
        {name: 'Telefone', content: '(81) 99975.5228', icon: 'fas fa-phone'},
        {name: 'Email', content: 'contato@whiteweddingcars.com.br', icon: 'fas fa-envelope'}
      ],
      social: [
        {icon: 'fab fa-facebook fa-3x', link: 'https://www.facebook.com/whiteweddingcar'},
        {icon: 'fab fa-instagram fa-3x', link: 'https://www.instagram.com/whiteweddingcars/'}
      ],
      message: ''
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
.space-container {
  margin-bottom: 3em;
  margin-top: 3em;
}
.custom-contact {
  margin-bottom: 3em;
}
.custom-contact h4 {
  margin-bottom: 1em;
}
.custom-contact a{
  margin-right: 2em;
  color: black;
}
.custom-contact a:hover{
  margin-right: 2em;
  color: rgba(0, 0, 0, 0.7);
}
.margin {
  margin-bottom: 3em;
}
h3 {
  font-family: 'Cormorant Garamond', serif;
  text-align: center;
  font-size: 72px
}
p{
  font-family: 'Raleway', sans-serif;
}
form{
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
@media (max-width: 991px) {
  .custom-contact {
    text-align: center;
  }
}
</style>
