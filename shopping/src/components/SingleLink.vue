<template>
  <router-link :to="link.path">{{ link.name }}</router-link>
</template>

<script>
export default {
  name: "singleLink",
  props: { link: Object },
};
</script>

<style scoped>
a.router-link-exact-active {
  border-bottom: solid 5px;
  border-image: linear-gradient(
      to right,
      hsl(136, 65%, 51%),
      hsl(192, 70%, 51%)
    )
    13;
  color: hsl(233, 26%, 24%);
}
a {
  text-decoration: none;
  padding: 28px 13px;
  margin: 0px 3px;
  color: hsl(233, 8%, 62%);
}
@media ((max-width: 910px) and (min-width: 800px )) {
  a {
    padding: 28px 10px;
    font-size: 15px;
  }
}
@media ((max-width: 800px )and (min-width: 700px)) {
  a {
    padding: 28px 6px;
    font-size: 14px;
  }
}
@media ((max-width: 700px) and (min-width: 600px)) {
  a {
    padding: 28px 3px;
    font-size: 13px;
  }
  a.router-link-exact-active {
    border-bottom: solid 4px;
  }
}
@media ((max-width: 600px) and (min-width:520px)) {
  a {
    padding: 28px 1px;
    font-size: 12px;
  }
}
</style>
