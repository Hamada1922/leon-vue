<template>
  <div class="contact">
    <section-title :head="head" :para="para" />
    <h2>Feel free to drop us a line at:</h2>
    <a href="#">leonagency@mail.com </a>
    <p>
      Find Us On Social Networks
      <i class="fab fa-youtube fa-fw"></i>
      <i class="fab fa-facebook-f fa-fw"></i>
      <i class="fab fa-twitter fa-fw"></i>
    </p>
  </div>
</template>
<script>
import SectionTitle from "@/components/SectionTitle.vue";
export default {
  name: "ContactView",
  data: function () {
    return {
      head: "Contact",
      para: "We are born to create",
    };
  },
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/_mixins.scss";
.contact {
  padding: 30px 0;
  text-align: center;
  h2 {
    font: {
      size: 35px;
    }
    color: var(--dark-torquoise);
    @include max-mobile {
      font-size: 25px;
    }
  }
  a {
    font: {
      size: 30px;
      weight: bold;
    }
    color: var(--torquoise);
    display: block;
    margin: 15px 0;
    @include max-mobile {
      font-size: 20px;
    }
  }
  p {
    color: var(--dark-torquoise);
    @include max-mobile {
      font-size: 14px;
    }
    i {
      cursor: pointer;
      transition: var(--transition);
      &:hover {
        transform: scale(1.2);
      }
    }
  }
}
</style>
