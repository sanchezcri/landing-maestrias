<template>
  <div class="container-sec-2">
    <div class="container mx-auto flex">
      <div
        class="section-2-part-2 w-1/3"
        @mouseover="cardHover = true"
        @mouseleave="cardHover = false"
      >
        <div class="card flex items-center justify-center p-4">
          <div class="">
            <div v-show="!cardHover" class="hide flex">
              <img
                :src="require(`~/assets/images/${items[0].icon}.png`)"
                class="image-card"
                alt=""
              />
              <p class="content-card m-auto">{{ items[0].content }}</p>
            </div>
          </div>
          <p v-show="cardHover">{{ items[0].hover }}</p>
        </div>
      </div>
      <div
        class="section-2-part-2 w-1/3"
        @mouseover="cardHover1 = true"
        @mouseleave="cardHover1 = false"
      >
        <div class="card flex items-center justify-center p-4">
          <div class="">
            <div v-show="!cardHover1" class="hide flex">
              <img
                :src="require(`~/assets/images/${items[1].icon}.png`)"
                class="image-card"
                alt=""
              />
              <p class="content-card m-auto">{{ items[1].content }}</p>
            </div>
          </div>
          <p v-show="cardHover1">{{ items[1].hover }}</p>
        </div>
      </div>
      <div
        class="section-2-part-2 w-1/3"
        @mouseover="cardHover2 = true"
        @mouseleave="cardHover2 = false"
      >
        <div class="card flex items-center justify-center p-4">
          <div class="">
            <div v-show="!cardHover2" class="hide flex">
              <img
                :src="require(`~/assets/images/${items[2].icon}.png`)"
                class="image-card"
                alt=""
              />
              <p class="content-card m-auto">{{ items[2].content }}</p>
            </div>
          </div>
          <p v-show="cardHover2">{{ items[2].hover }}</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      cardHover: false,
      cardHover1: false,
      cardHover2: false,
      items: [
        {
          icon: 'icon-1',
          content: 'ESCUELA #1 EN EL PERÚ',
          hover:
            'Escuela #1 en el Perú, tendrás el respaldo de una escuela top de América Latina y la única en Perú con la cuarta Corona Académica.',
        },
        {
          icon: 'icon-2',
          content: '#1 EN EL PERÚ TOP 10 EN LATINOAMERICA',
          hover:
            'Escuela #1 en el Perú, tendrás el respaldo de una escuela top de América Latina y la única en Perú con la cuarta Corona Académica.',
        },
        {
          icon: 'icon-3',
          content: '+5 PALMAS DE EXCELENCIA',
          hover:
            'Escuela #1 en el Perú, tendrás el respaldo de una escuela top de América Latina y la única en Perú con la cuarta Corona Académica.',
        },
      ],
    }
  },
}
</script>
<style scoped>
.container-sec-2 {
  cursor: pointer;
}
@media (max-width: 950px) {
  .container-sec-2 {
    display: none !important;
  }
}
.image-card {
  margin-right: 30px;
  width: 80px;
  height: auto;
}
.content-card {
  color: #363661;
  font-size: 24px;
  font-weight: 600;
  width: 174px;
}
.card {
  height: 20vh;
  font-size: 24px;
  background: #ffd700;
  border: none !important;
}
.card:hover {
  background: #e8ebf0;
}
.container-sec-2 {
  background: #ffd700;
}
.section-2-part-2 {
  height: 20vh;
}
</style>