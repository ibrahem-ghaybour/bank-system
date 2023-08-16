<template>
  <form @submit.prevent>
    <div
      class="input"
      v-for="typeInput in typeInputs"
      :key="typeInput.type"
      :id="typeInput.type"
    >
      <InputUser :obj="typeInput" />
    </div>
    <button id="login">Login</button>
  </form>
</template>

<script>
import InputUser from "./InputUser.vue";
export default {
  name: "formComponent",
  data() {
    return {
      typeInputs: [
        { type: "email", label: "Email addess" },
        { type: "password", label: "Password" },
        { type: "text", label: "UserName" },
        { type: "checkbox", label: "Agree with the idea of the site" },
      ],
    };
  },
  components: { InputUser },
};
</script>

<style scoped>
form {
  max-width: 400px;
  height: 500px;
  margin: auto;
  border-radius: 10px;
  display: flex;
  background: radial-gradient(circle, #15151779 0%, hsl(0, 0%, 100%) 100%);
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 0px 13px 5px rgba(0, 0, 0, 0.256);
}
.input {
  display: flex;
  flex-direction: column;
  width: 70%;
  margin: 10px 0px;
}
#checkbox {
  flex-direction: row-reverse;
  width: auto;
}
#login {
  padding: 8px 45px;
  border-radius: 15px;
  border: none;
  cursor: pointer;
  font-weight: bold;
  color: hsl(231, 11%, 37%);
  text-shadow: 0px 0px 2px hsl(231, 11%, 37%);
  background: #eee;
}
#login:hover {
  background: #fff;
}
@media (max-height: 500px) {
  form {
    height: 100%;
    margin: 0px auto;
  }
}
</style>
