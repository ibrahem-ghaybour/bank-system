<template>
  <h3>{{ text.titel }}</h3>
  <p>
    {{ text.details }}// f you're searching for ideas of products to sell
    online, it's a good idea to scope out Amazon's Movers and Shakers. That's
    where you'll find the sales ranking for every category in the e-commerce
    giant's marketplace. It helps to drill down to the categories you're most
    interested in and dig deep into the sales list to find unique fast movers.
    However, Amazon's offerings are often mass-market, high-volume items with
    wide distribution and stiff sales competition. Still, it can serve as
    inspiration.
  </p>
</template>

<script>
export default {
  name: "articlestext",
  props: {
    text: Object,
  },
};
</script>

<style scoped>
h3 {
  font-size: 20px;
  padding: 10px 0px;
  letter-spacing: 1px;
}
p {
  font-size: 15px;
  color: hsl(233, 8%, 62%);
  line-height: 20px;
  padding: 10px 0px;
}
@media (max-width: 636px) {
  h3 {
    padding: 6px 0px;
    letter-spacing: 0px;
  }
  p {
    font-size: 14px;
    line-height: 20px;
    padding: 0;
    padding-bottom: 5px;
  }
}
</style>
