<template>
  <div class="main-slider">
    <h3
      class="main-slider-title"
      data-aos="flip-left"
      v-html="content.title"
    ></h3>
    <div class="rectangle-orangle">
      <h4 class="main-slider-subtitle">{{ content.subtitle }}</h4>
    </div>
    <div id="btn-wrapper">
      <a href="#contactanos">
        <div class="registro-btn flex">
          <img src="~/assets/images/registro.png" class="img-reg mr-2" />
          <div class="flex m-auto"><p class="pt-2">REGISTRO</p></div>
        </div>
      </a>
      <img src="~/assets/images/main-slider-pj.png" class="img-mobile-bg" />
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      content: {
        title: 'CONVIÉRTETE <br>EN UN PROFESIONAL<br>DIFERENTE',
        subtitle: 'ESPECIALÍZATE, TRANSFORMA Y LIDERA',
      },
    }
  },
}
</script>
<style scoped>
#btn-wrapper {
  filter: drop-shadow(4px 10px 20px rgba(0, 0, 0, 0.25));
  height: 100vh;
}
.img-reg {
  height: 100%;
}
@media (max-width: 1000px) {
  .main-slider {
    height: auto !important;
  }
}
@media (min-width: 1000px) {
  .rectangle-orangle {
    padding: 25px 86px 27px 30px;
  }
}
@media (min-width: 851px) {
  .img-mobile-bg {
    display: none !important;
  }
}
@media (max-width: 850px) {
  .img-mobile-bg {
    position: absolute;
    bottom: 0;
  }
  .registro-btn {
    display: none !important;
  }
  .main-slider {
    background-position: right !important;
  }
  .rectangle-orangle {
    top: 25% !important;
    left: 18px !important;
  }
  .main-slider h3 {
    font-size: 2rem !important;
    line-height: 36px !important;
    top: 6% !important;
    left: 18px !important;
    position: relative;
    width: 322px !important;
  }
  .main-slider h4 {
    width: 300px !important;
    height: 76px !important;
    line-height: 24px !important;
    padding: 16px 32px 5px 16px;
  }
  .main-slider h4 {
    font-size: 1.33rem !important;
    position: relative !important;
  }
}
.registro-btn {
  position: absolute;
  right: 0;
  bottom: 59px;
  clip-path: polygon(0 0, 100% 0, 100% 100%, 11% 100%);
  background: #ff6401;
  box-shadow: 4px 10px 20px rgba(0, 0, 0, 0.25);
  color: white;
  padding: 17px 52px 12px 52px;
  font-size: 38px;
  font-weight: 600;
}
.rectangle-orangle {
  position: absolute;
  clip-path: polygon(0 0, 100% 0, 90% 100%, 0% 100%);
  background: linear-gradient(90deg, #ef3d00 -13.42%, #ff6400 116.42%);
  max-width: 38rem;
  max-height: 9rem;
  left: 50%;
  top: 46%;
}
.main-slider {
  position: relative;
  max-width: 100%;
  width: 100vw;
  height: 100vh;
  background: url('~assets/fondo-maestrias.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  font-weight: 600;
}
.main-slider h3 {
  font-size: 5rem;
  line-height: 72px;
  position: absolute;
  left: 50%;
  top: 20%;
  color: #3b69fa;
  width: auto;
  height: 216px;
}

.main-slider h4 {
  width: 600px;
  height: 115px;
  font-size: 3rem;
  line-height: 57px;
  color: #ffffff;
}
</style>