<template>
  <div class="footer-content">
    <div class="bg-footer"></div>
    <div class="bg-purple">
      <div class="section-redes text-center md:text-left mx-auto md:flex">
        <div class="w-full md:w-2/3">
          <h5 class="titleFooter">{{ title1 }}</h5>
          <div class="logos flex mx-auto pt-3 content-center md:content-start">
            <a
              v-for="social in socials"
              :key="social.icon"
              :href="social.url"
              class="icon-so"
            >
              <img
                :src="require(`~/assets/images/${social.icon}.png`)"
                class="logo-social"
              />
            </a>
          </div>
        </div>
        <div class="w-full md:w-1/3">
          <h5 class="titleFooter mt-6 md:mt-0">{{ title2 }}</h5>
          <div class="logos md:pt-3 flex mx-auto wsp-section">
            <img src="~/assets/images/wsp.png" class="wsp-icon" />
            <a :href="`tel:${wsp}`" class="wsp flex text-white">
              {{ wsp }}
            </a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      wsp: '(+51) 982 799 856',
      title1: 'Visita Nuestras Páginas',
      title2: 'Más Informes',
      socials: [
        {
          icon: 'fb',
          url: 'https://www.facebook.com',
        },
        {
          icon: 'twt',
          url: 'https://www.facebook.com',
        },
        {
          icon: 'yt',
          url: 'https://www.facebook.com',
        },
        {
          icon: 'link',
          url: 'https://www.facebook.com',
        },
      ],
    }
  },
}
</script>
<style scoped>
@media (min-width: 851px) {
  .titleFooter {
    text-align: left !important;
  }
}
@media (max-width: 850px) {
  .wsp {
    padding: 0 8px !important;
  }
  .wsp-section {
    margin-top: 9px !important;
  }
  .wsp-icon {
    width: 24px !important;
    height: 24px !important;
  }
  .titleFooter {
    font-size: 16px !important;
  }
  .wsp {
    font-size: 14px !important;
  }
  .logos {
    justify-content: center;
  }
}
.wsp {
  padding: 0 30px;
  margin: auto 0;
  font-size: 24px;
  font-weight: 400;
}

.icon-so {
  margin-right: 32px;
}
@media (min-width: 900px) {
  .wsp {
    padding: 0 30px;
    margin: auto 0;
    font-size: 24px;
    font-weight: 400x;
  }
}
.titleFooter {
  font-weight: 600;
  font-size: 24px;
  color: #ffffff;
}
.section-redes {
  padding: 66px 0px;
}
@media (min-width: 1000px) {
  .section-redes {
    max-width: 1100px;
  }
  .icon-so {
    margin-right: 50px;
    margin-top: 20px;
  }
}
.bg-footer {
  height: 4.4rem;
  background: linear-gradient(89.99deg, #ef3d00 -0.96%, #ff6400 99.98%);
}
.bg-purple {
  background: #363661;
}
</style>