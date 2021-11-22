<template>
  <div id="metodologia" class="bg-color">
    <div class="section-alianzas md:p-8 mx-auto">
      <h3 class="alianzas-title">{{ title }}</h3>
      <h4 class="alianzas-subtitle">{{ subtitle }}</h4>
      <div class="logos-aliados grid grid-cols-2 md:grid-cols-4 gap-6 md:gap-0">
        <div
          v-for="aliado in aliados.slice(0, 8)"
          :key="aliado.key"
          class="logos-aliado mx-auto"
        >
          <img
            :src="require(`~/assets/images/alianzas/${aliado.url}.png`)"
            class="text-center img-aliado mx-auto"
            :alt="aliado.alt"
          />
        </div>
      </div>
      <div class="logos-aliados grid grid-cols-3 md:grid-cols-3 gap-6 md:gap-0">
        <div
          v-for="aliado in aliados.slice(8, 12)"
          :key="aliado.key"
          class="logos-aliado mx-auto"
        >
          <img
            :src="require(`~/assets/images/alianzas/${aliado.url}.png`)"
            class="text-center img-aliado mx-auto"
            :alt="aliado.alt"
          />
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      title: 'METODOLOGÍA',
      subtitle: 'CON LAS MEJORES ALIANZAS',
      aliados: [
        {
          url: 'alianzas-logos-1',
          alt: 'centrum-pucp',
        },
        {
          url: 'alianzas-logos-2',
          alt: 'business school barcelona',
        },
        {
          url: 'alianzas-logos-3',
          alt: 'Georgetown University',
        },
        {
          url: 'alianzas-logos-4',
          alt: 'Florida International University',
        },
        {
          url: 'alianzas-logos-5',
          alt: 'Universidad Politécnica de Madrid',
        },
        {
          url: 'alianzas-logos-6',
          alt: 'Opus College of Business',
        },
        {
          url: 'alianzas-logos-7',
          alt: 'Politecnico Milano Gradute School Of Business',
        },
        {
          url: 'alianzas-logos-8',
          alt: 'Hec Montreal',
        },
        {
          url: 'alianzas-logos-9',
          alt: 'Arellano',
        },
        {
          url: 'alianzas-logos-11',
          alt: 'IE Business School',
        },
        {
          url: 'alianzas-logos-12',
          alt: 'Universidad Peruana Cayetano Heredida',
        },
      ],
    }
  },
}
</script>
<style scoped>
.logos-aliado {
  margin: auto !important;
}
@media (min-width: 851px) {
  .alianzas-subtitle {
    margin-bottom: 70px;
  }
  .img-alido {
    width: 90%;
    margin: auto !important;
  }
}
@media (max-width: 850px) {
  .img-aliado {
    width: 100% !important;
  }
  .section-alianzas {
    padding: 56px 41px 77px 41px !important;
  }
  .alianzas-subtitle {
    margin-bottom: 70px;
    font-size: 24px !important;
    line-height: 24px !important;
  }
  .alianzas-title {
    font-size: 36px !important;
  }
}
.section-alianzas h3 {
  font-weight: 600;
  font-size: 50px;
  color: #363661;
}
.section-alianzas h4 {
  font-size: 40px;
  color: #363661;
}
.logos-aliado {
  margin-bottom: 50px;
}
.section-alianzas {
  max-width: 1550px;
  padding: 8rem 0px 5rem 0px;
}
.bg-color {
  background: #e8ebf0;
}
</style>