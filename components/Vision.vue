<template>
  <div id="vision" class="section-tarjetas relative flex">
    <div class="md:flex container m-auto items-center">
      <div class="md:w-1/2 m-auto">
        <h2 class="title-s" v-html="title"></h2>
        <h3 class="subtitle-s mt-4 md:mt-0" v-html="subtitle"></h3>
        <h4 class="title2-s" v-html="title2"></h4>
        <p class="content-s" v-html="content"></p>
        <p class="content-s-mobile">{{ contentMobil }}</p>
      </div>
      <div class="md:w-1/2">
        <div class="tarjetas">
          <div
            v-for="tarjeta in tarjetas"
            :key="tarjeta.header"
            class="tarjeta"
            :class="tarjeta.color"
          >
            <h4 class="tarjeta-header">{{ tarjeta.header }}</h4>
            <p class="tarjeta-content">{{ tarjeta.txt }}</p>
          </div>
        </div>
      </div>
    </div>
    <img src="~/assets/images/img-sec-1.jpg" alt="" class="img-tarjetas" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      tarjetas: [
        {
          color: 'blue',
          header: '20%',
          txt: 'La satisfacción de un cliente aumenta hasta un 20 % de media si su KAM se ha formado en un programa de gestión de cuentas clave',
        },
        {
          color: 'orange',
          header: '70%',
          txt: 'La satisfacción de un cliente aumenta hasta un 20 % de media si su KAM se ha formado en un programa de gestión de cuentas clave',
        },
        {
          color: 'red',
          header: '58%',
          txt: 'La satisfacción de un cliente aumenta hasta un 20 % de media si su KAM se ha formado en un programa de gestión de cuentas clave',
        },
      ],
      title: 'MEJORA<br>TU VISIÓN',
      subtitle: 'ALCANZA TUS METAS',
      title2: 'Impulsa tu carrera con un MAESTRIA ESPECIALIZADA.<br> <br>',
      content:
        'Donde los conocimientos gerenciales del<br>nuevo mundo se integran con contenidos <br>innovadores bajo un modelo flexible que<br>se adapta a tu estilo de vida y lleva al<br>siguiente nivel tu carrera profesional.<br><br> ¡Transforma tu manera de ver y hacer<br>negocios!',
      contentMobil:
        'Donde los conocimientos gerenciales del nuevo mundo se integran con contenidos innovadores bajo un modelo flexible que se adapta a tu estilo de vida y lleva al siguiente nivel tu carrera profesional.¡Transforma tu manera de ver y hacer negocios!',
    }
  },
}
</script>
<style scoped>
@media (min-width: 1200px) {
  .title2-s {
    width: 386px;
  }
}
@media (min-width: 850px) {
  .img-tarjetas {
    position: absolute;
    width: 47% !important;
    top: 0;
    right: 0;
  }
}
@media (min-width: 851px) {
  .content-s-mobile {
    display: none;
  }
}
@media (max-width: 850px) {
  .title-s {
    font-size: 32px !important;
    line-height: 29px !important;
  }
  .img-tarjetas {
    display: none;
  }
  .content-s-mobile {
    padding-bottom: 22px;
  }
  .content-s {
    display: none;
  }
  .subtitle-s {
    font-size: 28px !important;
    margin-top: -5px;
    padding-bottom: 15px;
  }
  .title2-s {
    font-size: 24px !important;
    line-height: 24px !important;
  }
  .section-tarjetas {
    height: auto !important;
    padding: 60px 32px 60px 41px;
  }
  .tarjeta-header {
    font-size: 36px !important;
  }
  .tarjeta {
    width: 100% !important;
    font-size: 14px !important;
    padding: 22px 32px 15px 32px !important;
  }
  .tarjetas {
    position: relative !important;
  }
}
.tarjetas {
  position: absolute;
  bottom: 0px;
  z-index: 2;
}
.tarjeta {
  margin-bottom: 24px;
}
.title2-s {
  color: #363661;
  font-weight: 600;
  font-size: 32px;
}
.content-s {
  font-size: 24px;
  line-height: 39px;
}
.subtitle-s {
  font-size: 40px;
  color: #3b69fa;
}
.section-tarjetas {
  height: 95vh;
}
.title-s {
  font-size: 4rem;
  font-weight: 600;
  color: #3b69fa;
  line-height: 57px;
}
.tarjeta-header {
  font-size: 64px;
  font-weight: 600;
  text-align: center;
}
.tarjeta {
  max-width: 472px;
  color: white;
  font-size: 20px;
  padding: 32px 40px 32px 56px;
}
.blue {
  background: #3b69fa;
}
.orange {
  background: #ff6400;
}
.red {
  background: #ef3d00;
}
</style>