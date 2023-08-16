<template>
  <div class="detailsArticle">
    <RemoveButton @click="showData" />
    <img :src="articles[index].img" />
    <ArticlesText :text="articles[index]" />
  </div>
</template>
<script>
import ArticlesText from "./ArticlesText.vue";
import RemoveButton from "./RemoveButton.vue";
export default {
  name: "detailsAritcle",
  props: {
    articles: Object,
    index: Number,
  },
  data() {
    return {
      show: true,
      text: {
        titel: "Figure out your after-tax income:",
        details:
          " If you get a regular paycheck, the amount you receive is probably it, but if you have automatic deductions for a 401(k), savings, and health and life insurance, add those back in to give yourself a true picture of your savings and expenditures. If you have other types of income — perhaps you make money from side gigs — subtract anything that reduces it, such as taxes and business expenses.",
      },
    };
  },
  mounted() {
    this.show = this.detailsShow;
  },
  methods: {
    showData() {
      this.show = false;
      this.$emit("boolean", this.show);
    },
  },
  components: { ArticlesText, RemoveButton },
};
</script>
<!-- TODO:amendment style responsive-->
<style scoped>
.detailsArticle {
  position: absolute;
  width: 40%;
  height: 500px;
  padding: 10px;
  background: hsl(233, 29%, 39%);
  border-radius: 15px;
  overflow: hidden;
  color: #fff;
  margin: auto;
}
img {
  width: 100%;
  height: 40%;
  object-fit: cover;
  border-radius: 15px;
}
@media (max-width: 636px) {
  .detailsArticle {
    width: 310px;
  }
  img {
    height: 28%;
  }
}
</style>
