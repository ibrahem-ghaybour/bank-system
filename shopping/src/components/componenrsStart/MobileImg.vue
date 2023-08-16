<template>
  <div>
    <ModileBackground />
    <img src="../../assets/images/image-mockups.png" class="mobile" />
  </div>
</template>
<script>
import ModileBackground from "./ModileBackground.vue";
export default {
  components: { ModileBackground },
};
</script>

<style scoped>
.mobile {
  width: 750px;
  position: absolute;
  top: -100px;
  left: -20px;
}
div {
  width: 50%;
  position: relative;
}

@media ((max-width: 900px) and (min-width:520px)) {
  div {
    width: 40%;
    left: 20%;
    top: 10%;
  }
}
@media (max-width: 520px) {
  div {
    width: 70%;
    top: -10%;
    left: -65%;
  }
  .mobile {
    width: 100%;
    position: absolute;
    top: 0px;
    left: 0px;
  }
}
</style>
