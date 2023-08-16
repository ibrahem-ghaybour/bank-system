<template>
  <!-- TODO:amendment action -->
  <form
    action="mailto:ebrahimghaibour65@gmail.com?"
    method="post"
    enctype="text/plain"
  >
    <input v-model="email" type="email" placeholder="user email" required />
    <input v-model="password" type="password" placeholder="Password" required />
    <textarea
      v-model="message"
      name="message"
      cols="20"
      rows="5"
      placeholder="Message"
      required
    ></textarea>
    <button>Submit</button>
  </form>
</template>
<script>
import InputUser from "../componentsLogin/InputUser.vue";
export default {
  name: "detailsMessage",
  data() {
    return {
      a: "",
      email: "",
      password: "",
      message: "",
    };
  },
  methods: {
    a(event) {
      this.password = event;
    },
    b(event) {
      this.email = event;
    },
  },
  components: { InputUser },
};
</script>

<style scoped>
form {
  top: 40%;
  right: 0;
  width: 250px;
  height: 270px;
  margin: 10px 0px;
  border-radius: 10px;
  display: flex;
  background: radial-gradient(
    circle,
    hsl(231, 36%, 85%) 0%,
    hsl(136, 65%, 51%) 100%
  );
  flex-direction: column;
  justify-content: center;
  align-items: center;
  box-shadow: 0px 0px 13px 5px rgba(0, 0, 0, 0.256);
  overflow: hidden;
}
input,
textarea {
  width: 70%;
  padding: 7px 0px;
  margin: 3px 0px;
  border: none;
  border-radius: 5px;
  outline: none;
  background: #b4edbe;
  color: hsl(0, 1%, 38%);
}
button {
  padding: 5px 35px;
  border: none;
  border-radius: 20px;
  cursor: pointer;
  background: linear-gradient(to left, hsl(136, 65%, 51%), hsl(192, 70%, 51%));
  color: #fff;
  font-size: 15px;
  transition: 0.5s;
  margin-top: 10px;
}
button:hover {
  scale: 1.05;
  background: linear-gradient(to left, hsla(136, 65%, 51%, 0.829), hsla(192, 70%, 51%, 0.741));

}
</style>
