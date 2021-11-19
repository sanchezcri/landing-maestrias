<template>
  <div
    class="flex items-center"
    @mouseover="cardHover = true"
    @mouseleave="cardHover = false"
  >
    <div class="w-1/3 grid grid-cols-2">
      <img :src="require(`~/assets/images/${icon}.png`)" alt="" />
      <p>{{ title }}</p>
      <p v-show="cardHover">{{ hover }}</p>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    icon: {
      type: String,
      default: '',
    },
    hover: {
      type: String,
      default: '',
    },
    title: {
      type: String,
      default: '',
    },
  },
  data() {
    return {}
  },
}
</script>