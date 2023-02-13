<template>
  <div class="portfolio">
    <section-title :head="head" :para="para" />
    <div class="container">
      <div class="card">
        <img src="@/assets/portfolio-1.png" alt="card" />
        <div class="text">
          <h4>Project Here</h4>
          <p>
            My creative ability is very difficult to measure because it can
            manifest in so many surprising and
          </p>
        </div>
      </div>
      <div class="card">
        <img src="@/assets/portfolio-2.png" alt="card" />
        <div class="text">
          <h4>Project Here</h4>
          <p>
            My creative ability is very difficult to measure because it can
            manifest in so many surprising and
          </p>
        </div>
      </div>
      <div class="card">
        <img src="@/assets/portflio-3.png" alt="card" />
        <div class="text">
          <h4>Project Here</h4>
          <p>
            My creative ability is very difficult to measure because it can
            manifest in so many surprising and
          </p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import SectionTitle from "@/components/SectionTitle.vue";
export default {
  name: "PortfolioView",
  data: function () {
    return {
      head: "Portfolio",
      para: "If you do it right, it will last forever",
    };
  },
  components: {
    SectionTitle,
  },
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/_mixins.scss";
.portfolio {
  padding: 30px 0;
  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    gap: 30px;
    @include max-mobile {
      flex-direction: column;
    }
    .card {
      padding: 20px;
      @include max-mobile {
        text-align: center;
      }
      img {
        max-width: 100%;
      }
      h4 {
        margin: 10px 0;
      }
      p {
        color: var(--para);
        @include max-small {
          font-size: 14px;
        }
      }
    }
  }
}
</style>
