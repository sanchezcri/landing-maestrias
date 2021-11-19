<template>
  <b-navbar
    toggleable="lg"
    type="dark"
    sticky
    class="
      flex flex-row
      navbar
      justify-center
      md:justify-between
      items-center
      sticky
    "
  >
    <div>
      <img src="~/assets/images/LOGO-PUCP.png" alt="" class="logo-pucp" />
    </div>
    <div class="items-center nav-items">
      <ul class="flex flex-row items-navbar items-center">
        <li v-for="item in menu" :key="item.title" :class="item.class">
          <a :href="item.href">
            {{ item.title }}
          </a>
        </li>
      </ul>
    </div>
  </b-navbar>
</template>
<script>
export default {
  data() {
    return {
      menu: [
        {
          title: 'MEJORA TU VISIÓN',
          class: '',
          href: '#vision',
        },
        {
          title: 'OBJETIVOS',
          class: '',
          href: '#objetivos',
        },
        {
          title: 'METODOLOGIA',
          class: '',
          href: '#metodologia',
        },
        {
          title: 'REGISTRO',
          class: 'li-registro',
          href: '#contactanos',
        },
      ],
    }
  },
}
</script>
<style scoped>
a:hover {
  color: white !important;
  text-decoration: none !important;
}
@media (max-width: 1250px) {
  .nav-items {
    display: none !important;
  }
  .navbar {
    padding: 12px 0px !important;
    justify-content: center !important;
  }
  .logo-pucp {
    width: 68px !important;
  }
}
.li-registro {
  background: #ff6401;
  clip-path: polygon(0 0, 100% 0, 86% 100%, 0 100%);
  padding: 3px 28px 0px 22px;
}
.items-navbar li {
  margin-left: 83px;
}
.navbar {
  background: #363661;
  padding: 38px 10rem 38px 10rem;
  color: #eaeaea;
  font-size: 22px;
  font-weight: 500;
}
.logo-pucp {
  max-width: 227px;
}
</style>
