<template>
  <img src="../../assets/images/bg-intro-desktop.svg" id="desktop_" />
  <img src="../../assets/images/bg-intro-mobile.svg" id="mobiel_" alt="" />
</template>
<style scoped>
img {
  position: absolute;
  width: 1050px;
  top: -210px;
  left: -150px;
  z-index: -1;
}
#mobiel_ {
  display: none;
}
@media (max-width: 520px) {
  #mobiel_ {
    display: block;
  }
  #desktop_ {
    display: none;
  }
  img{
  width:100%;
  top: 0px;
  left: -7px;
  }
}
</style>
