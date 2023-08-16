<template>
  <div class="navparMain">
    <div class="logo">
      <LogoNavpar />
    </div>
    <!-- TODO training (!) -->
    <ul :class="{ translat: click }">
      <li v-for="(link, index) in links" :key="index">
        <SingleLink :link="link"></SingleLink>
      </li>
    </ul>
    <RequestInviteButton id="button" />
    <button v-if="!click" id="click" @click="click = !click">
      <span><img src="../assets/images/icon-hamburger.svg" alt="" /></span>
    </button>
    <button v-else id="close" @click="showNavpar">
      <span><img src="../assets/images/icon-close.svg" alt="" /></span>
    </button>
  </div>
</template>

<script>
import LogoNavpar from "./LogoNavpar.vue";
import SingleLink from "./SingleLink.vue";
import RequestInviteButton from "./RequestInviteButton.vue";
export default {
  name: "navparMain",
  data() {
    return {
      links: [
        { name: "Home", path: "/" },
        { name: "About", path: "/about" },
        { name: "Contact", path: "/contact" },
        { name: "Blog", path: "/blog" },
        { name: "Careers", path: "/careers" },
        { name: " Request Invite", path: "/requestInvite" },
      ],
      click: false,
    };
  },
  components: { LogoNavpar, SingleLink, RequestInviteButton },
  //TODO:new avent
  mounted() {
    // window.addEventListener("resize", this.onResize);
  },
  methods: {
    // onResize() {
    //   window.innerWidth > 520 ? (this.click = true) : (this.click = false);
    // },
    showNavpar() {
      this.click = !this.click;
    },
  },
};
</script>

<style scoped>
.navparMain,
ul {
  display: flex;
  align-items: center;
}
li {
  list-style-type: none;
}
.navparMain {
  position: sticky;
  top: 0;
  width: 100%;
  height: 85px;
  justify-content: space-evenly;
  background: hsl(0, 0%, 100%);
  z-index: 12;
  box-shadow: 0px 0px 10px 3px rgba(0, 0, 0, 0.579);
}
#close,
#click {
  display: none;
}
@media (max-width: 520px) {
  .navparMain {
    justify-content: space-between;
    height: 65px;
  }
  #button {
    display: none;
  }
  ul {
    flex-direction: column;
    position: absolute;
    align-items: center;
    top: -500px;
    width: 75%;
    left: 12.5%;
    height: 320px;
    background: hsl(0, 0%, 100%);
    border-radius: 10px;
    transition: 0.4s;
  }
  .translat {
    transition: 0.5s;
    box-shadow: 0px 80px 100px 30px rgba(0, 0, 0, 0.705);
    top: 115%;
  }
  a,
  li {
    padding: 15px 13px;
    margin: 0px 4px;
  }
  #click,
  #close {
    border: none;
    background: fixed;
    cursor: pointer;
    margin-right: 20px;
    display: block;
  }
  .logo {
    margin-left: 20px;
  }
}
</style>
