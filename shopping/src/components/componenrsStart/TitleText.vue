<template>
  <div class="text">
    <h2 class="titel" :class="{ hoverClass: hover }" :style="font">
      {{ text.titel }}
    </h2>
    <p class="detailsText" :style="style_p">
      {{ text.details }}
    </p>
  </div>
</template>
<script>
export default {
  name: "titleText",
  // TODO:amendment is props
  props: {
    text: Object,
    font: String || "",
    style_p: String || "",
    hover: Boolean || "",
  },
};
</script>

<style scoped>
div {
  width: 40%;
  text-align: left;
  padding: 10px;
  margin-left: 80px;
}
div h2 {
  margin-bottom: 20px;
  color: hsl(233, 26%, 24%);
  font-weight: 400;
}
div p {
  margin: 30px 0px;
  color: hsl(233, 8%, 62%);
  line-height: 30px;
}
.hoverClass:hover {
  color: hsl(192, 70%, 51%);
}
@media (max-width: 900px) {
  div h1 {
    margin-bottom: 15px;
    font-size: 40px;
  }
  div p {
    margin: 20px 0px;
    line-height: 25px;
  }
  div {
    width: 45%;
    margin-left: 40px;
  }
}
@media (max-width: 520px) {
  div {
    width: 90%;
    margin: auto;
    padding: 0;
    text-align: center;
  }
}
</style>
