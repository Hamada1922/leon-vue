<template>
  <div class="about">
    <section-title :head="head" :para="para" />
    <div class="container">
      <div class="image">
        <img src="@/assets/about.png" alt="about" />
      </div>
      <div class="text">
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil nemo
          neque voluptate tempora velit cum non, fuga vitae architecto delectus
          sed maxime rerum impedit aliquam obcaecati, aut excepturi iusto
          laudantium!
        </p>
        <hr />
        <p>
          Lorem ipsum dolor sit amet consectetur adipisicing elit. Nihil nemo
          neque voluptate tempora velit cum non, fuga vitae architecto delectus
          sed maxime rerum impedit aliquam obcaecati, aut excepturi iusto
          laudantium!
        </p>
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "@/components/SectionTitle.vue";

export default {
  name: "AboutView",
  data: function () {
    return {
      head: "About",
      para: "Less is more work",
    };
  },
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/_mixins.scss";
.about {
  padding: 30px 0;
  .container {
    display: flex;
    align-items: center;
    @include max-mobile {
      flex-direction: column;
      gap: 40px;
      text-align: center;
    }
    .image {
      max-width: 35%;
      position: relative;
      &::before {
        position: absolute;
        content: "";
        top: 50%;
        transform: translateY(-50%);
        left: 0;
        width: 25%;
        height: 110%;
        background-color: var(--dark-torquoise);
        z-index: -1;
      }
      img {
        max-width: 90%;
      }
    }
    .text {
      p {
        max-width: 95%;
        @include max-mobile {
          font-size: 12px;
        }
      }
      p:last-of-type {
        color: var(--para);
      }
      hr {
        width: 50%;
        margin: 30px 0;
        height: 3px;
        background-color: var(--torquoise);
        @include max-mobile {
          margin: 30px auto;
        }
      }
    }
  }
}
</style>
