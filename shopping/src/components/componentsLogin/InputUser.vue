<template>
  <label :for="obj.type">{{ obj.label }}</label>
  <input
    v-model="dataInput"
    :class="obj.type"
    :type="obj.type"
    required
  />
</template>

<script>
export default {
  name: "inputUser",
  props: {
    obj: Object,
  },
  data() {
    return {
      dataInput: "",
    };
  },
};
</script>

<style scoped>
label {
  color: hsl(233, 26%, 24%);
  font-weight: 400;
  font-size: 15px;
  padding: 5px 0px;
}
input {
  width: 100%;
  padding: 10px 0px;
  padding-left: 5px;
  border: none;
  border-radius: 5px;
  outline: none;
  background: #ffffff;
  color: hsl(233, 26%, 24%);
}
.checkbox {
  width: 20px;
  margin-right: 10px;
  clip-path: circle(33% at 50% 50%);
  accent-color: rgb(154, 59, 192);
  cursor: pointer;
}
</style>
