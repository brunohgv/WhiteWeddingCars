<template>
  <div class="vertical-space parallax">
  </div>
</template>

<script>
export default {
}
</script>

<style scoped>
.vertical-space{
  height: 100vh;
}
.parallax {
  height: 50vh;
  background-image: url('../assets/SAL_4957.jpg');
  /* Create the parallax scrolling effect */
  background-attachment: fixed;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  filter: brightness(0.2) sepia(1)
}
</style>
