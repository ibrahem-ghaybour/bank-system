<template>
  <div class="aricle">
    <img :src="article.img" alt="" />
    <p class="author">{{ article.author }}</p>
    <TitleText :hover="true" :text="article" :font="font" :style_p="style_p" />
  </div>
</template>

<script>
import TitleText from "../componenrsStart/TitleText.vue";
export default {
  name: "article",
  props: { article: Object },
  data() {
    return {
      font: "font-size:20px",
      style_p: "line-height:20px; padding:0px;margin-top:-12px",
    };
  },
  components: { TitleText },
};
</script>

<style scoped>
.text {
  text-align: left;
  margin: 0;
  width: 85%;
  margin: auto;
  padding: 0%;
}

.aricle {
  width: 310px;
  height: 400px;
  text-align: left;
  overflow: hidden;
  background: rgb(210, 174, 238);
  background: radial-gradient(
    circle,
    rgb(255, 255, 255) 0%,
    rgba(221, 223, 237, 1) 100%
  );
  border-radius: 5px;
  margin: 10px 0px;
  cursor: pointer;
}
img {
  width: 100%;
  height: 50%;
  margin: auto;
  border-radius: 5px;
  object-fit: cover;
}
.author {
  font-size: 13px;
  color: hsl(233, 8%, 62%);
  margin: 5px 0px;
  margin-left: 25px;
}
</style>
