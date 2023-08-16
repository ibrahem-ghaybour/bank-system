<template>
  <div class="login">
    <FormComponent />
  </div>
</template>

<script>
import FormComponent from "./FormComponent.vue";
export default {
  name: "loginUser",
  components: { FormComponent },
};
</script>

<style scoped>
.login {
  width: 100%;
  height: 100vh;
  background: url("../../assets/images/pexels-optical-chemist-15873666.jpg");
  background-size: cover;
  padding-top: 50px;
}
</style>
