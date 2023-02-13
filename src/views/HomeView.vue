<template>
  <div>
    <section class="home">
      <div class="text">
        <h1>Hello There</h1>
        <p>We are Leon - Super Creative & Minimal Agency Web Template</p>
      </div>
    </section>
    <div class="features">
      <div class="container">
        <div class="feat">
          <i class="fas fa-magic fa-3x"></i>
          <h3>Tell Us Your Idea</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut lab
          </p>
        </div>
        <div class="feat">
          <i class="far fa-gem fa-3x"></i>
          <h3>Tell Us Your Idea</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut lab
          </p>
        </div>
        <div class="feat">
          <i class="fas fa-globe-asia fa-3x"></i>
          <h3>Tell Us Your Idea</h3>
          <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do
            eiusmod tempor incididunt ut lab
          </p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  components: {},
};
</script>
<style scoped lang="scss">
@import "src/scss/helpers/_mixins.scss";
.home {
  position: relative;
  background: url("@/assets/mountains.avif") no-repeat top center;
  background-size: cover;
  min-height: calc(100vh - 70px);
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  .text {
    text-align: center;
    h1 {
      color: var(--torquoise);
      font-size: 40px;
    }
    p {
      color: var(--white);
      margin-top: 20px;
      max-width: 300px;
    }
  }
}
.features {
  background-color: #f6f6f6;
  padding: 50px 0;
  .container {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 30px;
    text-align: center;
    @include max-mobile {
      grid-template-columns: repeat(auto-fill, minmax(250px, 1fr));
    }
    .feat {
      i {
        color: var(--torquoise);
      }
      h3 {
        margin: 20px 0;
      }
      p {
        color: var(--para);
        max-width: 100%;
      }
    }
  }
}
</style>
