<template>
  <header>
    <div class="container">
      <img src="@/assets/logo.png" alt="logo" class="logo" />
      <nav>
        <ul class="menu">
          <router-link to="/"><a>Home</a></router-link>
          <router-link to="/services"><a>Services</a></router-link>
          <router-link to="/portfolio"><a>Portfolio</a></router-link>
          <router-link to="/about"><a>About</a></router-link>
          <router-link to="/contact"><a>Contact</a></router-link>
        </ul>
        <button class="toggler" @click="toggler()">
          <span></span>
          <span></span>
          <span></span>
        </button>
      </nav>
    </div>
  </header>
</template>

<script>
export default {
  name: "MainHeader",
  methods: {
    toggler: function () {
      document.querySelector(".menu").classList.toggle("active");
    },
  },
};
</script>

<style lang="scss" scoped>
@import "src/scss/helpers/mixins";
header {
  background-color: var(--white);
  .container {
    display: flex;
    align-items: center;
    justify-content: space-between;
    border-bottom: 1px solid var(--head-title);
    .logo {
      max-height: 70px;
      padding: 10px 0;
    }
    nav {
      ul {
        display: none;
        &.active {
          display: flex;
          position: absolute;
          right: 0;
          top: 100%;
          flex-direction: column;
          background: #999;
          width: 200px;
          gap: 1px;
          z-index: 2;
          @include max-mobile {
            width: 100%;
          }
          a {
            display: block;
            background: #f6f6f6;
            padding: 7px 5px;
            color: var(--dark-torqouise);
            transition: var(--transition);
            &:hover {
              padding-left: 20px;
            }
          }
        }
      }
      .toggler {
        display: flex;
        width: 30px;
        flex-direction: column;
        align-items: flex-end;
        background: transparent;
        gap: 3px;
        span {
          height: 3px;
          background-color: var(--para);
        }
        span:not(:nth-of-type(2)) {
          width: 100%;
        }
        span:nth-of-type(2) {
          width: 60%;
          transition: var(--transition);
        }
        &:hover {
          span:nth-of-type(2) {
            width: 100%;
          }
        }
      }
    }
  }
}
</style>
