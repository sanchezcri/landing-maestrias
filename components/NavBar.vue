<template>
  <b-navbar
    toggleable="lg"
    type="dark"
    sticky
    class="navbar justify-center md:justify-between items-center"
  >
    <div class="content-nav flex justify-between">
      <div>
        <img src="~/assets/images/LOGO-PUCP.png" alt="" class="logo-pucp" />
      </div>
      <div class="flex items-center nav-items">
        <ul class="flex flex-row items-navbar items-center">
          <li v-for="item in menu" :key="item.title" :class="item.class">
            <a :href="item.href">
              {{ item.title }}
            </a>
          </li>
        </ul>
      </div>
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
  padding: 5px 28px 0px 22px;
  margin-bottom: 5px;
}
.items-navbar li {
  margin-left: 4.4rem;
}
.content-nav {
  width: 80%;
  margin: auto;
}
.navbar {
  background: #363661;
  padding: 45px 1rem 43px 1rem;
  color: #eaeaea;
  font-size: 22px;
  font-weight: 500;
}
.logo-pucp {
  max-width: 227px;
}
</style>
