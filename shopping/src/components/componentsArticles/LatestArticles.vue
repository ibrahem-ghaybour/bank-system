<template>
  <div class="allArticles">
    <!-- TODO: Event data -->
    <div
      class="details"
      :style="{ top: `${topArticle}px` }"
      :class="{ detailsN: !detailsShow, detailsShow: detailsShow }"
    >
      <DetailsArticle
        @boolean="getData"
        :articles="articles"
        :index="indexDetails"
      />
    </div>
    <h2 class="titelArticles">Latest Articles By</h2>
    <div class="aricles">
      <!-- TODO:how amendment data automatically -->
      <div
        ref="details"
        v-for="(article, index) in articles"
        :key="index"
        @click="viewDetails({ ele: 'details', index })"
      >
        <ArticleComponent :article="article" />
      </div>
    </div>
  </div>
</template>

<script>
import ArticleComponent from "@/components/componentsArticles/ArticleComponent.vue";
import DetailsArticle from "./DetailsArticle.vue";
//...........imgs...........Articles
import currency from "@/assets/images/image-currency.jpg";
import restaurant from "@/assets/images/image-restaurant.jpg";
import plane from "@/assets/images/image-plane.jpg";
import confetti from "@/assets/images/image-confetti.jpg";

export default {
  name: "latesAricles",
  data() {
    return {
      topArticle: 0,
      indexDetails: 0,
      detailsShow: false,
      articles: [
        {
          author: "By Claire Robinson",
          titel: "Receive money in any currency with no fees",
          img: currency,
          details:
            "The world isgetting smaller and we’re becoming more mobile. So why should you be forced to only receive money in a single … ",
        },
        {
          author: "By Wilson Hutton",
          titel: "Treat yourself without worrying about money",
          img: restaurant,
          details:
            "Our simple budgeting feature allows you to separate out your spending and set realistic limits each month. That means you … ",
        },
        {
          author: "By Wilson Hutton",
          titel: "Take your Easybank card wherever you go",
          img: plane,
          details:
            "We want you to enjoy your travels. This is why we don’t charge any fees on purchases while you’re abroad. We’ll even show you … ",
        },
        {
          author: "By Claire Robinson",
          titel: "Our invite-only Beta accounts are now live!",
          img: confetti,
          details:
            " After a lot of hard work by the whole team, we’re excited to launch our closed beta. It’s easy to request an invite through the site ... ",
        },
      ],
    };
  },
  methods: {
    getData(event) {
      this.detailsShow = event;
    },
    viewDetails({ ele, index }) {
      this.detailsShow = true;
      this.indexDetails = index;
      this.translateDetails({ ele, index });
    },
    translateDetails({ ele, index }) {
      if (window.innerWidth <= 636)
        this.topArticle =
          this.$refs[ele][index].getBoundingClientRect().height * index + 100;
      // else if (window.innerWidth > 636) {
      //   this.topArticle = 0;
      //   this.leftArticle =
      //     this.$refs[ele][index].getBoundingClientRect().width * index;
      // }
      else this.topArticle = 20;
    },
  },
  components: { ArticleComponent, DetailsArticle },
};
</script>

<style scoped>
.allArticles {
  width: 100%;
  background: hsl(0, 0%, 98%);
}
.aricles {
  width: 100%;
  height: 100%;
  display: flex;
  align-items: top;
  justify-content: space-evenly;
  flex-wrap: wrap;
  padding: 60px 0px;
}
.titelArticles {
  font-size: 30px;
  text-align: left;
  padding-left: 60px;
  padding-top: 20px;
  color: hsl(233, 10%, 35%);
}
.details {
  transition: 0.5s;
  width: 100%;
  margin-top: auto;
  position: relative;
}
.detailsShow {
  transition: 0.5s;
  left: 30%;
}
.detailsN {
  transition: 0.5s;
  left: 100%;
}

@media ((min-width: 637px) and (max-width:1256px)) {
  .detailsShow {
    left: 58%;
    transform: translateY(200px);
  }
  .detailsN {
    left: 100%;
  }
}
@media (max-width: 636px) {
  .titelArticles {
    text-align: center;
    padding-left: 0px;
  }
  .details {
    display: flex;
    justify-content: center;
  }
  .detailsShow {
    transition: 0.5s;
    left: 0%;
  }
}
</style>
<!-- -->
