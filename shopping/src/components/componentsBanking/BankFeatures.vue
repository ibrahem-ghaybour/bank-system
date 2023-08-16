<template>
  <div>
    <img :src="feature.img" alt="" />
    <TitleText :text="feature" :font="font" />
  </div>
</template>

<script>
import TitleText from "../componenrsStart/TitleText.vue";
export default {
  name: "bankFeatures",
  props: {
    feature: Object,
  },
  data() {
    return {
      font: "font-size:25px",
    };
  },
  components: { TitleText },
};
</script>

<style scoped>
.text {
  width: 100%;
  margin: 0;
  margin-right: 5px;
}
@media (max-width: 690px) {
  .text {
    margin: 10px 0px;
    text-align: center;
  }
}
</style>
