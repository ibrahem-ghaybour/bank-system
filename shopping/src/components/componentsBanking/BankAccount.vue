<template>
  <div id="bankAll">
    <TitleText :text="text" :font="font" />
    <div class="features">
      <div class="feature" v-for="(feature ,index) in features" :key="index">
        <BankFeatures :feature="feature" />
      </div>
    </div>
  </div>
</template>

<script>
import TitleText from "../componenrsStart/TitleText.vue";
import BankFeatures from "./BankFeatures.vue";
//imgs......................
import Online from "../../assets/images/icon-online.svg";
import Simple from "../../assets/images/icon-budgeting.svg";
import Fast from "../../assets/images/icon-onboarding.svg";
import OPenApi from "../../assets/images/icon-api.svg";
export default {
  name: "bankAccount",
  data() {
    return {
      font: "font-size:40px;",
      text: {
        titel: "Why choose Easybank?",
        details:
          " We leverage Open Banking to turn your bank account intoyour financial hub. Control your finances link never before ",
      },
      features: [
        {
          titel: "Online Banking",
          img: Online,
          details:
            "Our modern web and mobile applications allow you to keep track of yourfinances wherever you are in the world.",
        },
        {
          titel: "Simple Budgeting",
          img: Simple,
          details:
            "See exactly where your money goes each month. Receive notifications when you’re close to hitting your limits.",
        },
        {
          titel: "Fast Onboarding",
          img: Fast,
          details:
            "We don’t do branches. Open your account in minutes online and start taking control of your finances right away.",
        },
        {
          titel: "Open API",
          img: OPenApi,
          details:
            "Manage your savings, investments, penstion, and much more from one account. Tracking your money has never been easier",
        },
      ],
    };
  },
  components: { TitleText, BankFeatures },
};
</script>

<style scoped>
#bankAll {
  width: 100%;
  background: hsl(220, 16%, 96%);
  padding-top: 100px;
}
.features {
  width: 80%;
  margin: 0px auto;
  display: flex;
  justify-content: space-evenly;
  align-items: top;
  text-align: left;
  flex-wrap: wrap;
}
.feature {
  width: 250px;
  margin: 10px;
}
@media (max-width: 690px) {
  .features {
    text-align: center;
  }
  #bankAll {
    padding-top: 20px;
  }
}
</style>
