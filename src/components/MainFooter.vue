<template>
  <footer>
    <p>&copy; 2022 <span>Leon</span> all rights reserved</p>
    <p>redesigned by <span>SiniGami</span></p>
  </footer>
</template>

<script>
export default {
  name: "MainFooter",
};
</script>

<style lang="scss" scoped>
footer {
  bottom: 0;
  padding: 30px 0;
  background-color: var(--dark-torquoise);
  color: var(--white);
  text-align: center;
  font-weight: bold;
  span {
    color: var(--torquoise);
  }
}
</style>
