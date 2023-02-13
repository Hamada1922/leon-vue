<template>
  <div class="main-heading">
    <h2>{{ head }}</h2>
    <p>{{ para }}</p>
  </div>
</template>

<script>
export default {
  props: ["head", "para"],
  name: "SectionTitle",
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/_mixins.scss";

.main-heading {
  text-align: center;
  margin-bottom: 50px;
  h2 {
    font-size: 90px;
    color: var(--head-title);
    @include max-mobile {
      font-size: 50px;
    }
  }
  p {
    color: var(--para);
    font-size: 18px;
    transform: translateY(-35px);
    @include max-mobile {
      font-size: 12px;
      transform: translateY(-20px);
    }
  }
}
</style>
