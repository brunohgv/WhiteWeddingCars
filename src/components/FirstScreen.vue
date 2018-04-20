<template>
  <div class="height">
    <!-- start of first content -->
    <div class="cover-img">
      <b-img class="grayscale image-inside" :src="image" alt=""/>
      <div class="filter"></div>
      <div class="text-inside">
        <!-- testar com tag p em negrito -->
        <h2>VOCÊ MERECE CHEGAR</h2>
        <h1>DESLUMBRANTE</h1>
        <h2>EM SEU GRANDE DIA</h2>
      </div>
    </div>
    <!-- end of first content -->
    <!-- start of second content -->
      <!-- <home-services-component></home-services-component> -->
    <!-- end of second content -->
  </div>
</template>

<script>
import image from '@/assets/LMT_0149.jpg'
export default {
  data () {
    return {
      image: image
    }
  }
}
</script>

<style scoped>
.cover-img {
  font-family: 'Cormorant Garamond', serif;
  width: 100%;
  height: 100%;
}
.image-inside {
  position: relative;
  object-fit: cover;
  width: 100%;
  height: 100vh;
  left: 0;
  right: 0;
}
.text-inside {
  z-index: 20;
  position: absolute;
  left: 50%;
  top: 50vh;
  transform: translate(-50%, -50%);
  color: white;
  text-align: center;
}
.grayscale {
  /* -webkit-filter: grayscale(0.5);
  filter: grayscale(0.5); */
  -webkit-filter: brightness(.6);
  filter: brightness(.6);
}
h2, h1 {
  font-family: 'Cormorant Garamond', serif;
  margin: 0;
}
h2 {
  font-size: 36px
}
h1{
  font-size: 124px
}
@media (max-width: 960px) {
  h2 {
    font-size: 30px
  }
  h1 {
    font-size: 72px
  }
}
@media (max-width: 720px) {
  h2 {
    font-size: 24px
  }
  h1 {
    font-size: 62px
  }
}
@media (max-width: 540px) {
  h2 {
    font-size: 22px
  }
  h1 {
    font-size: 44px
  }
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
