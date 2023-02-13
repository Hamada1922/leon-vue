<template>
  <div class="services-sec">
    <section-title head="services" para="Don't be busy, be productive" />
    <div class="container">
      <div class="services">
        <div class="service">
          <i class="fas fa-palette fa-2x"></i>
          <div class="text">
            <h3>Graphic Design</h3>
            <p>
              Graphic design is the process of visual communication and
              problem-solving using one or more of typography, photography and
              illustration
            </p>
          </div>
        </div>
        <div class="service">
          <i class="fab fa-sketch fa-2x"></i>
          <div class="text">
            <h3>Graphic Design</h3>
            <p>
              Graphic design is the process of visual communication and
              problem-solving using one or more of typography, photography and
              illustration
            </p>
          </div>
        </div>
        <div class="service">
          <i class="fas fa-vector-square fa-2x"></i>
          <div class="text">
            <h3>Graphic Design</h3>
            <p>
              Graphic design is the process of visual communication and
              problem-solving using one or more of typography, photography and
              illustration
            </p>
          </div>
        </div>
        <div class="service">
          <i class="fas fa-pencil-ruler fa-2x"></i>
          <div class="text">
            <h3>Graphic Design</h3>
            <p>
              Graphic design is the process of visual communication and
              problem-solving using one or more of typography, photography and
              illustration
            </p>
          </div>
        </div>
      </div>
      <div class="image">
        <img src="@/assets/services.png" alt="services" />
      </div>
    </div>
  </div>
</template>

<script>
import SectionTitle from "@/components/SectionTitle.vue";

export default {
  name: "ServicesView",
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/mixins";
.services-sec {
  padding: 30px 0;
}
.container {
  display: flex;
  align-items: center;
  gap: 30px;
  @include max-small {
    flex-direction: column;
  }
  .services {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    gap: 30px;
    @include max-small {
      grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    }
    .service {
      display: flex;
      gap: 20px;
      @include max-mobile {
        flex-direction: column;
        align-items: center;
      }
      .text {
        @include max-mobile {
          text-align: center;
        }
      }
      i {
        color: var(--torquoise);
      }
      p {
        margin-top: 20px;
        color: var(--para);
        font-size: 14px;
        max-width: 90%;
      }
    }
  }
  .image {
    max-width: 35%;
    position: relative;
    @include max-mobile {
      max-width: 90%;
    }
    &::after {
      position: absolute;
      content: "";
      right: 0;
      top: 50%;
      transform: translateY(-50%);
      width: 25%;
      height: 110%;
      background-color: var(--dark-torquoise);
      z-index: -1;
    }
    img {
      max-width: 90%;
    }
  }
}
</style>
