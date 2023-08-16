<template>
  <div :class="{ show: showScroll, n_show: !showScroll }">
    <DetailsMessageUser :class="{ showForm: click, n_showForm: !click }" />
    <ButtonWithUser @click="click = !click" title="Mail communication" />
  </div>
</template>

<script>
import ButtonWithUser from "./ButtonWithUser.vue";
import DetailsMessageUser from "./DetailsMessageUser.vue";
export default {
  name: "connectWithUser",
  components: { ButtonWithUser, DetailsMessageUser },
  data() {
    return {
      click: false,
      showScroll: false,
    };
  },
  methods: {
    myScrollFunc() {
      let y = window.scrollY;
      if (y >= 500) {
        this.showScroll = true;
      } else {
        this.showScroll = false;
      }
    },
  },
  mounted() {
    window.addEventListener("scroll", this.myScrollFunc);
  },
};
</script>

<style scoped>
div {
  position: fixed;
  top: 80%;
  right: 0;
  text-align: right;
  padding: 10px;
  transition: 1s;
  z-index: 121;
}
/* TODO: name class amendment*/
.n_showForm {
  position: absolute;
  transition: 0.5s;
  opacity: 0;
  right: -300%;
  top: -350%;
}
.showForm {
  position: absolute;
  transition: 0.5s;
  opacity: 1;
  right: 0%;
  top: -350%;
}

.n_show {
  opacity: 0;
  right: -100%;
}
.show {
  opacity: 1;
  right: 0%;
}
</style>
