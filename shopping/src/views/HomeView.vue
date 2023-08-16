<template>
  <div class="home">
    <SectionOne />
    <DetailsMessageUser />
    <BankAccount />
    <LatestArticles />

    <!--. 
           
    About Us Contact Blog Careers Support Privacy Policy Request
    Invite © Easybank. All Rights Reserved -->
  </div>
</template>
<script>
import SectionOne from "@/components/componenrsStart/SectionOne.vue";
import BankAccount from "@/components/componentsBanking/BankAccount.vue";
import LatestArticles from "@/components/componentsArticles/LatestArticles.vue";
import DetailsMessageUser from "@/components/componentsConnectWithUs/ConnectWithUser.vue";

export default {
  name: "HomeView",
  components: { SectionOne, BankAccount, LatestArticles, DetailsMessageUser },
};
</script>

<style scoped>
.home {
  width: 100%;
  position: relative;
  overflow: hidden;
}
</style>
