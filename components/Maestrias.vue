<template>
  <div class="section-maestrias">
    <div class="container mx-auto">
      <h3 class="maestrias-title">{{ title }}</h3>
      <div class="cursos grid grid-cols-4 gap-4">
        <div
          v-for="curso in cursos.slice(0, 8)"
          :key="curso.index"
          class="titulo"
        >
          <h3>
            {{ curso.titulo }}
          </h3>
          <a :href="curso.url">VER</a>
        </div>
      </div>
      <div class="cursos line-2 grid grid-cols-4 gap-4">
        <div></div>
        <div
          v-for="curso in cursos.slice(8, 10)"
          :key="curso.index"
          class="titulo"
        >
          <h3>
            {{ curso.titulo }}
          </h3>
          <a :href="curso.url">VER</a>
        </div>
        <div></div>
      </div>
      <div
        v-if="slide == 1"
        class="cursos-mobile mobile-1 grid grid-rows-4 grid-flow-col gap-4"
      >
        <div
          v-for="curso in cursos.slice(0, 4)"
          :key="curso.index"
          class="titulo"
        >
          <h3 class="titulo-curso">
            {{ curso.titulo }}
          </h3>
          <a :href="curso.url" class="curso-link">VER</a>
        </div>
      </div>
      <transition name="slide-fade">
        <div
          v-if="slide == 2"
          class="cursos-mobile mobile-1 grid grid-rows-4 grid-flow-col gap-4"
        >
          <div
            v-for="curso in cursos.slice(4, 8)"
            :key="curso.index"
            class="titulo"
          >
            <h3 class="titulo-curso">
              {{ curso.titulo }}
            </h3>
            <a :href="curso.url" class="curso-link">VER</a>
          </div>
        </div>
      </transition>
      <div
        v-if="slide == 3"
        class="cursos-mobile mobile-1 grid grid-rows-4 grid-flow-col gap-4"
      >
        <div
          v-for="curso in cursos.slice(8, 12)"
          :key="curso.index"
          class="titulo"
        >
          <h3 class="titulo-curso">
            {{ curso.titulo }}
          </h3>
          <a :href="curso.url" class="curso-link">VER</a>
        </div>
      </div>
      <div class="btn-zone text-center m-4">
        <span
          :class="{ active: slide == 1 }"
          class="btn-cursos"
          @click="slide = 1"
        ></span>
        <span
          :class="{ active: slide == 2 }"
          class="btn-cursos"
          @click="slide = 2"
        ></span>
        <span
          :class="{ active: slide == 3 }"
          class="btn-cursos"
          @click="slide = 3"
        ></span>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      slide: 1,
      title: 'Elige entre las diferentes MAESTRÍAS ESPECIALIZADAS',
      cursos: [
        {
          titulo: 'DIRECCIÓN DE MARKETING',
          url: '#',
        },
        {
          titulo: 'Dirección de Finanzas Corporativas y Riesgos Financieros',
          url: '#',
        },
        {
          titulo: 'Tecnología de la Información',
          url: '#',
        },
        {
          titulo: 'Dirección Estratégica de Talento',
          url: '#',
        },
        {
          titulo: 'Supply Chain Management',
          url: '#',
        },
        {
          titulo: 'Dirección de Operaciones Productivas',
          url: '#',
        },
        {
          titulo: 'Gerencia del Desarrollo Competitivo Regional',
          url: '#',
        },
        {
          titulo: 'Administración Estratégica de Negocios Jurídicos',
          url: '#',
        },
        {
          titulo:
            'Gestión y Dirección de Empresas Constructoras e Inmobiliarias',
          url: '#',
        },
        {
          titulo: 'Administración de la Energía',
          url: '#',
        },
      ],
    }
  },
}
</script>
<style scoped>
.btn-zone {
  padding-top: 20px;
}
.active {
  background: #ffd700 !important;
}
@media (min-width: 851px) {
  .cursos-mobile,
  .btn-zone {
    display: none !important;
  }
}
@media (max-width: 850px) {
  .cursos-mobile {
    padding: 0px 40px;
  }
  .curso-link {
    font-size: 14px !important;
    padding-top: 20px !important;
  }
  .maestrias-title {
    font-size: 24px !important;
    line-height: 24px !important;
    padding-bottom: 15px !important;
  }
  .section-maestrias {
    padding: 60px 39px !important;
  }
  .titulo {
    padding: 15px 30px 10px 30px !important;
    background-position: top right !important;
  }
  .titulo-curso {
    font-size: 14px !important;
    line-height: 14px !important;
  }
  .cursos {
    display: none;
  }
  .section-maestrias {
    height: auto !important;
    background-position: center !important;
  }
}
.btn-cursos {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  border: 2px solid #ffd700;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}
.line-2 {
  margin-top: 1rem;
}
.titulo {
  text-align: center;
  max-width: 348px;
  max-height: 217px;
  background: url('~/assets/images/titulo-bg.jpg');
  padding: 70px 45px 25px 45px;
}
.titulo h3 {
  font-size: 1.44rem;
  font-weight: 600;
  color: #ffffff;
  line-height: 24.7px;
}
.titulo a {
  font-size: 24px;
  color: #ffd700;
  padding-top: 23px;
  font-weight: 400;
  text-decoration: underline;
}
.maestrias-title {
  color: white;
  font-size: 36px;
  font-weight: 600;
  padding-bottom: 5rem;
}
.section-maestrias {
  height: auto;
  width: 100vw;
  max-width: 100%;
  /* background-image: url('~assets/images/material-maestrias.jpg'); */
  background: linear-gradient(
      90.1deg,
      rgba(54, 54, 97, 0.95) 0.08%,
      rgba(255, 100, 0, 0.855) 99.9%
    ),
    url('~assets/images/material-maestrias.jpg');
  background-size: cover;
  background-repeat: no-repeat;
  padding: 6.4rem 0;
}
</style>