<template>
  <div class="divstyle">
    <b-container>
      <b-row class="justify-content-md-center row-class">
        <b-col md="4" sm="12" xs="12" class="col-class">
          <b-img src="../assets/logo.png" class="max-height" fluid></b-img>
        </b-col>
        <b-col md="4" sm="12" xs="12" class="col-class">
          <div class="col-content">
            <h4>White Wedding Cars</h4>
            <div class="custom-contact">
              <h4>{{ contactMessage }}</h4>
              <p v-for="option in contactOptions" :key="option.name"><i :class="option.icon"></i> {{option.content}}</p>
            </div>
            <div class="custom-contact">
              <a v-for="media in social" :key="media.icon" :href="media.link" target="_blank"><i :class="media.icon"></i></a>
            </div>
          </div>
        </b-col>
      </b-row>
    </b-container>
  </div>
</template>

<script>
export default {
  data () {
    return {
      contactOptions: [
        {name: 'Telefone', content: '(81) 99975.5228', icon: 'fas fa-phone'},
        {name: 'Email', content: 'contato@whiteweddingcars.com.br', icon: 'fas fa-envelope'}
      ],
      social: [
        {icon: 'fab fa-facebook fa-2x', link: 'https://www.facebook.com/whiteweddingcar'},
        {icon: 'fab fa-instagram fa-2x', link: 'https://www.instagram.com/whiteweddingcars/'}
      ],
    }
  }
}
</script>

<style>
.divstyle{
  background-color: #000;
  color: white;
  text-align: center;
  margin: 0;
}
.custom-contact a{
  color: white;
  margin-left: 0.5em;
  margin-right: 0.5em; 
}
.custom-contact a:hover{
  color: rgba(255, 255, 255, 0.7);
}
.custom-contact p{
  margin-bottom: 0.2rem;
}
.col-class {
  display: flex;
  flex-direction: column;
  padding-top: 3em; 
  padding-bottom: 3em;
}
.col-content {
  align-self: center;
}
.row-class {
  display: flex;
  align-items: center;
}
</style>
