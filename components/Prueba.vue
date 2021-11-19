<template>
  <div id="prueba" ref="prueba">
    <div class="flex items-center relative">
      <div class="w-full md:w-3/5"></div>
      <div class="w-full md:w-2/5 column-prueba md:flex items-center my-auto">
        <div class="content-column-prueba">
          <h2 class="font-semibold text-white prueba-title">
            {{ pruebaTitle }}
          </h2>
          <h3 class="font-medium text-white prueba-subtitle">
            {{ pruebaSubtitle }}
          </h3>
          <div class="flex space">
            <div class="w-1/2 md:w-full"></div>
            <div class="w-1/2 md:w-full">
              <p class="text-white txt-prueba">
                {{ pruebaTxt }}
              </p>
            </div>
          </div>
          <div class="btn-wrapper">
            <button
              @click="comenzarPrueba()"
              class="text-white btn-comenzar-prueba"
            >
              COMENZAR PRUEBA
            </button>
          </div>
        </div>
      </div>
      <img src="~/assets/images/img-prueba.png" class="img-prueba" />
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      prueba: false,
      puntaje: 0,
      step: 0,
      pruebaTitle: 'Es sorprendente todo lo que puedes alcanzar',
      pruebaSubtitle:
        'Pon a prueba tus conocimientos y diferenciate de los demás',
      pruebaTxt:
        'Lo que diferencia a un profesional es la formación, descubre tus habilidades y potencialos.',
      headerPrueba: '¡Elige tu futuro y diferénciate!',
      preguntas: [
        {
          question:
            'Colocar la pregunta que no sobrepase dos líneas máximo para ser conciso.',
          details: '',
          alternative1: 'Alternativa 1',
          alternative2: 'Alternativa 2',
          alternative3: 'Alternativa 3',
        },
      ],
    }
  },
  methods: {
    comenzarPrueba() {
      console.log('Hi')
      document.getElementById('prueba').style.background =
        "url('https://dc688.4shared.com/img/EQBlg4Doiq/s24/17d39befa48/test-bg?async&rand=0.8192420697061247')"
      // this.$refs.prueba.style.animationName = 'bg'
    },
  },
}
</script>
<style scoped>
@media (max-width: 350px) {
  .space {
    margin-top: 5rem !important;
  }
}
.img-prueba {
  position: absolute;
  bottom: 7%;
  width: 60%;
  left: -5%;
}
@media (min-width: 850px) {
  .prueba-title {
    width: 350px;
  }
  .img-prueba {
    width: auto;
    bottom: 0;
    left: 18%;
  }
}
.btn-comenzar-prueba:hover {
  background: #ff6400 !important;
  color: #ffd700 !important;
}
@media (max-width: 850px) {
  .img-prueba {
    bottom: 0 !important;
  }
  .btn-wrapper {
    position: absolute !important;
    left: 5% !important;
  }
  .column-prueba {
    height: auto !important;
  }
  .space {
    margin-top: 12rem;
  }
  .btn-comenzar-prueba {
    font-size: 18px !important;
    padding: 12px 108px 9px 13px !important;
  }
  #prueba {
    padding: 60px 0px;
  }
  .txt-prueba {
    width: 117px !important;
    font-size: 14px !important;
    line-height: 14px !important;
  }
  .prueba-title {
    font-size: 32px !important;
    line-height: 32px !important;
  }
  .prueba-subtitle {
    font-size: 24px !important;
    line-height: 24px !important;
    width: 277px !important;
  }
}

.btn-comenzar-prueba {
  font-weight: 600;
  font-size: 18px;
  color: #ff6400 !important;
  clip-path: polygon(0 0, 100% 0%, 76% 100%, 0% 100%);
  background: #ffd700;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25) !important;
  padding: 25px 156px 16px 32px;
  text-align: left;
}
.txt-prueba {
  font-size: 24px;
  line-height: 28px;
  width: 410px;
  margin-bottom: 40px;
}
.column-prueba {
  height: 100vh;
}
.prueba-title {
  font-size: 42px;
  line-height: 40px;
  margin-bottom: 40px;
}
#prueba {
  max-width: 100%;
  width: 100vw;
  height: 100vh;
  background: linear-gradient(
      112deg,
      rgba(2, 0, 36, 0) 0%,
      rgba(9, 9, 121, 0) 19%,
      rgba(8, 35, 139, 0) 30%,
      rgba(1, 3, 13, 0) 90%,
      rgba(255, 100, 0, 1) 90%,
      rgba(0, 0, 0, 0.29735644257703087) 100%
    ),
    url('~assets/images/bg-prueba.jpg');
  background-size: cover;
  background-repeat: no-repeat;
}
.prueba-subtitle {
  font-size: 32px;
  line-height: 30px;
  width: 420px;
  margin-bottom: 40px;
}
.btn-wrapper {
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
  position: relative;
  z-index: 10;
}
@keyframes bg {
  from {
    background: linear-gradient(
        112deg,
        rgba(2, 0, 36, 0) 0%,
        rgba(9, 9, 121, 0) 35%,
        rgba(8, 35, 139, 0) 88%,
        rgba(255, 115, 0, 0.753) 91%,
        rgb(255, 115, 0) 100%
      ),
      url('~assets/images/bg-prueba.jpg');
  }
  to {
    background: linear-gradient(
        112deg,
        rgba(255, 94, 0, 0) 0%,
        rgba(255, 94, 0, 0) 19%,
        rgba(255, 94, 0, 0) 30%,
        rgb(255, 115, 0) 39%,
        rgb(255, 115, 0) 100%
      ),
      url('~assets/images/bg-prueba.jpg');
  }
}
</style>