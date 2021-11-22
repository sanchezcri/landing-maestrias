<template>
  <div id="objetivos" class="bg-color relative">
    <div class="row md:flex adn-section items-center container mx-auto">
      <div class="header-mobile">
        <h2 class="adn-title">{{ adnTitle }}</h2>
        <h3 class="adn-subtitle">{{ adnSubtitle }}</h3>
      </div>
      <div class="w-full md:w-1/3">
        <div v-for="section in sections.slice(0, 3)" :key="section.main">
          <div class="row flex mobile-reverse">
            <div class="w-4/5 md:w-2/3 side-left">
              <h3 class="adn-feature-title">{{ section.main }}</h3>
              <!-- eslint-disable vue/no-v-html -->
              <p class="adn-content" v-html="section.content"></p>
              <!--eslint-enable-->
            </div>
            <div class="w-1/5 md:w-1/3">
              <img
                :src="require(`~/assets/images/adn/${section.icon}.png`)"
                class="img-vision"
              />
            </div>
          </div>
        </div>
      </div>
      <div class="w-full md:w-1/3 text-center content-titles">
        <h2 class="adn-title">{{ adnTitle }}</h2>
        <h3 class="adn-subtitle">{{ adnSubtitle }}</h3>
      </div>
      <div class="w-full md:w-1/3 row-content">
        <div v-for="section in sections.slice(3, 7)" :key="section.main">
          <div class="row flex">
            <div class="w-1/5 md:w-1/3">
              <img
                :src="require(`~/assets/images/adn/${section.icon}.png`)"
                class="img-vision"
              />
            </div>
            <div class="w-4/5 md:w-2/3 side-right">
              <h3 class="adn-feature-title">{{ section.main }}</h3>
              <!-- eslint-disable vue/no-v-html -->
              <p class="adn-content" v-html="section.content"></p>
              <!--eslint-enable-->
            </div>
          </div>
        </div>
      </div>
      <a href="#contactanos">
        <button class="pulse-button">
          <img
            src="~/assets/images/adn/adn-arrow.png"
            class="m-auto img-arrow"
          />
        </button>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      adnTitle: 'ADN CENTRUM',
      adnSubtitle: 'LO QUE NOS HACE DIFERENTES',
      sections: [
        {
          main: 'CERTIFICACIONES',
          content:
            'Grado de Magíster y Certificación Internacional Simultánea.',
          icon: 'adn-icon-1',
        },
        {
          main: 'ALIANZAS ESTRATÉGICAS',
          content:
            'Mantenemos una alianza  con la consultora líder en empleabilidad, Lee Hecht Harrisson – DBM, para asesorar tu búsqueda de mejora profesional. Si eres alumno o graduado, podrás buscar en las bolsas laborales, las ferias laborales.',
          icon: 'adn-icon-2',
        },
        {
          main: 'PRESTIGIO ACADÉMICO',
          content:
            ' <ul class="list-disc list-inside"> <li>Excelencia Docente</li> <li>Formación continua con cursos gratuitos.</li>  <li>Voluntariado Mentoring.</li> </ul>',
          icon: 'adn-icon-3',
        },
        {
          main: 'STAGE INTERNACIONAL',
          content:
            'Semana académica al campus de Eada Business School Barcelona. Incluye una semana de clases en la Universidad.',
          icon: 'adn-icon-4',
        },
        {
          main: 'EMPLEABILIDAD',
          content:
            'Viaje al centro de formación de alto rendimiento en Barcelona para recibir clases intensivas por Eada Business School.',
          icon: 'adn-icon-5',
        },
        {
          main: 'NETWORKING',
          content:
            '<ul class="list-disc list-inside"><li>Networking Internacional</li> <li>Red Profesional con más de 9 mil Alumnos.</li></ul>',
          icon: 'adn-icon-6',
        },
        {
          main: 'MALLA CURRICULAR',
          content:
            'Malla Curricular de Impacto, alineada al MBA con cursos gerenciales, incluye Taller de Human Growth, Método del Caso.',
          icon: 'adn-icon-7',
        },
      ],
    }
  },
}
</script>
<style scoped>
.arrow {
  background-image: url('~/assets/images/adn/adn-arrow.png');
  background-size: contain;
  background-repeat: no-repeat;
}
@media (min-width: 851px) {
  .header-mobile {
    display: none !important;
  }
  .pulse-button {
    bottom: 4%;
    left: calc(52% - 90px) !important;
  }
}
@media (max-width: 850px) {
  .img-arrow {
    width: 60% !important;
  }
  .pulse-button {
    width: 46px !important;
    height: 46px !important;
  }
  .container-btn {
    bottom: 0 !important;
    left: 40% !important;
    top: 90% !important;
  }
  .side-right {
    margin-bottom: 25px !important;
  }
  .side-left {
    margin-bottom: 25px !important;
  }
  .adn-content {
    font-size: 14px !important;
    line-height: 14.4px !important;
  }
  .adn-feature-title {
    font-size: 14px !important;
  }
  .img-vision {
    width: 46px !important;
    height: auto;
  }
  .mobile-reverse {
    flex-direction: row-reverse;
  }
  .row-content {
    flex-direction: row-reverse !important;
  }
  .adn-title {
    font-size: 24px !important;
    text-align: center;
  }
  .adn-subtitle {
    font-size: 18px !important;
    line-height: 18px !important;
    text-align: center;
    padding-bottom: 30px !important;
  }
  .content-titles {
    display: none !important;
  }
  .adn-section {
    height: auto !important;
    padding: 49px 40px 150px 40px;
  }
}
.adn-content {
  line-height: 22px;
  font-size: 18px;
  color: #363661;
}
.adn-feature-title {
  font-size: 24px;
  font-weight: 600;
  color: #363661;
}
.adn-title {
  font-size: 50px;
  font-weight: 600;
  color: #ff6400;
}
.adn-subtitle {
  font-size: 40px;
  line-height: 40px;
  color: #363661;
}
.side-right {
  margin-bottom: 65px;
}
.side-left {
  margin-bottom: 80px;
}
.adn-section {
  height: 95vh;
}
.bg-color {
  background: #e8ebf0;
}
.container-btn {
  width: 200px;
  height: 200px;
  margin: 0 auto 0;
  position: absolute;
  top: 80%;
  left: 48%;
}

.pulse-button {
  position: absolute;
  bottom: 4%;
  left: 40%;
  width: 100px;
  height: 100px;
  border: none;
  box-shadow: 0 0 0 0 rgba(232, 76, 61, 0.7);
  border-radius: 50%;
  background: linear-gradient(90deg, #ef3d00 0%, #ff6400 108.33%);

  cursor: pointer;
  -webkit-animation: pulse 1.25s infinite cubic-bezier(0.66, 0, 0, 1);
  -moz-animation: pulse 1.25s infinite cubic-bezier(0.66, 0, 0, 1);
  -ms-animation: pulse 1.25s infinite cubic-bezier(0.66, 0, 0, 1);
  animation: pulse 1.25s infinite cubic-bezier(0.66, 0, 0, 1);
}

@-webkit-keyframes pulse {
  to {
    box-shadow: 0 0 0 45px rgba(232, 76, 61, 0);
  }
}
@-moz-keyframes pulse {
  to {
    box-shadow: 0 0 0 45px rgba(232, 76, 61, 0);
  }
}
@-ms-keyframes pulse {
  to {
    box-shadow: 0 0 0 45px rgba(232, 76, 61, 0);
  }
}
@keyframes pulse {
  to {
    box-shadow: 0 0 0 45px rgba(232, 76, 61, 0);
  }
}
</style>