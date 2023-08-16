<template>
  <div id="section">
    <div id="tt">
      <TitleText :text="text" class="titelSite" :font="font" />
      <div id="button"><RequestInviteButton /></div>
    </div>
    <MobileImg id="imgs" />
  </div>
</template>
<!-- TODO:Modify the iPad style -->
<script>
import RequestInviteButton from "../RequestInviteButton.vue";
import MobileImg from "./MobileImg.vue";
import TitleText from "./TitleText.vue";
export default {
  name: "sectionOne",
  data() {
    return {
      font: "font-size: 50px",
      text: {
        titel: "Next generation digital banking",
        details:
          "Take your financial life online. Your Easybank account will be aone-stop-shop for spending, saving, budgeting, investing, and much more.",
      },
    };
  },
  components: { RequestInviteButton, MobileImg, TitleText },
};
</script>

<style scoped>
#section {
  width: 100%;
  height: 100vh;
  display: flex;
  align-items: center;
  justify-content: left;
  /* background: hsl(0, 0%, 100%); */
  overflow: hidden;
}
#imgs {
  position: absolute;
  top: 0;
  left: 60%;
}
#button {
  width: 30%;
  text-align: left;
  padding: 10px;
  margin-left: 80px;
}
@media (max-width: 900px) {
  #button {
    width: 45%;
    margin-left: 40px;
  }
}
@media (max-width: 520px) {
  #section {
    align-items: end;
  }
  #button {
    width: 90%;
    margin: auto;
    padding: 0;
    text-align: center;
    margin-bottom: 50px;
    /* width: 90%;
    margin: auto;
    padding: 0;
    margin-top: 10px;
    text-align: center; */

    /* margin-bottom: 100px; */
  }
  #imgs {
    width: 100%;
    position: absolute;
    translate: -59% -50px;
    /* width: 100%;
    position: absolute;
    transform: translate(-59%, -50px); */

    /* width: 100%;
    position: relative;
    top:-50px;
    left: 2%; */
  }
}
@media (max-width: 376px) {
  #section {
    height: 118vh;
  }
}
</style>
