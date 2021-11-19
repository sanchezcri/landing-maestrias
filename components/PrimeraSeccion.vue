<template>
  <div class="section-1-part-1 flex relative items-center">
    <div class="w-full md:w-2/3">
      <div class="rectangle-blue">
        <h4 class="primera-seccion-header pt-3 md:pt-0" v-html="header"></h4>
      </div>
    </div>
    <div class="w-full md:w-1/3 content-pr">
      <div class="mobile-facts flex">
        <div class="w-1/2">
          <div v-for="iconmob in iconsmob" :key="iconmob.txt" class="flex pt-4">
            <div class="w-1/3">
              <img :src="require(`~/assets/images/${iconmob.img}.png`)" />
            </div>
            <div class="w-2/3">
              <p>{{ iconmob.txt }}</p>
            </div>
          </div>
        </div>
      </div>
      <h3 v-html="title"></h3>
      <p class="pt-3 md:pt-0" v-html="content"></p>
    </div>
    <img src="~/assets/images/section-2pj.png" alt="" class="pj-section-1" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'Impulsa tu carrera con un<br>MAESTRIA ESPECIALIZADA.',
      content:
        'Donde los conocimientos gerenciales del <br>nuevo mundo se integran con contenidos<br>innovadores bajo un modelo flexible que<br>se adapta a tu estilo de vida y lleva al<br>siguiente nivel tu carrera profesional.<br><br> ¡Transforma tu manera de ver y hacer negocios!',
      header: '<strong>ELIGE UNA MAESTRÍA</strong><br>ELIGE TU FUTURO',
      iconsmob: [
        {
          img: 'mobile-icon-1',
          txt: 'ESCUELA #1 EN EL PERÚ',
        },
        {
          img: 'mobile-icon-2',
          txt: '#1 EN EL PERÚ TOP 10 EN LATINOAMERICA',
        },
        {
          img: 'mobile-icon-3',
          txt: '+5 PALMAS DE EXCELENCIA',
        },
      ],
    }
  },
}
</script>
<style scoped>
@media (min-width: 850px) {
  .mobile-facts {
    display: none;
  }
  .pj-section-1 {
    position: absolute;
    bottom: 0;
    left: 38%;
  }
}
@media (max-width: 850px) {
  .mobile-facts {
    padding-top: 15px;
    padding-bottom: 25px;
  }
  .rectangle-blue {
    left: 0 !important;
  }
  .pj-section-1 {
    display: none !important;
  }
  .content-pr p {
    font-size: 14px !important;
    line-height: 14px !important;
  }
  h3 {
    font-size: 24px !important;
    line-height: 24px !important;
  }
  .primera-seccion-header {
    font-size: 18px !important;
    line-height: 22px !important;
  }
  .rectangle-blue {
    position: relative !important;
    padding: 17px 40px 17px 16px !important;
  }
  .section-1-part-1 {
    display: block !important;
    height: auto !important;
    padding: 60px 41px 72px 41px;
  }
}
.mobile-facts p {
  font-weight: 600;
  font-size: 14px;
  color: #ffd700;
}
.rectangle-blue {
  padding: 64px 40px 51px 43px;
  position: absolute;
  clip-path: polygon(0 0, 100% 0, 90% 100%, 0% 100%);
  background: #3b69fa;
  left: 10%;
  top: 30%;
}
h4 {
  font-size: 56px;
  line-height: 57px;
  color: #ffffff;
}
h3 {
  font-weight: 600;
  font-size: 32px;
}
p {
  font-size: 32px;
  font-weight: 400;
}
.section-1-part-1 {
  height: 80vh;
  background: linear-gradient(90deg, #ef3d00 -102.24%, #ff6400 90.38%);
  color: white;
}
</style>