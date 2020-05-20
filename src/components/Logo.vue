<template>
  <div class="logo">
    <router-link to="/">code ahead<span class="curser">_</span></router-link>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss">
@use "../assets/styles/abstracts/abstracts";
.logo {
  margin: 1rem;
  font-size: 2rem;
  font-family: abstracts.$font-logo;
  align-self: flex-start;
  a {
    color: abstracts.$text-main;
    text-decoration: none;
  }
  .curser {
    animation: blinker 1s linear infinite;
  }

  @keyframes blinker {
    50% {
      opacity: 0;
    }
  }
}
</style>
