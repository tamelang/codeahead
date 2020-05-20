<template>
  <header>
    <div class="navbar">
      <Logo></Logo>
      <button
        class="hamburger"
        v-bind:class="{
          'hamburger--collapse': displayFlyout,
          'is-active': displayFlyout,
        }"
        type="button"
        @click="toggleFlyout"
      >
        <span class="hamburger-box">
          <span class="hamburger-inner"></span>
        </span>
      </button>
    </div>
    <div class="nav flyout" v-bind:class="{ 'is-active': displayFlyout }">
      <div>
        <router-link to="/about">About me</router-link>
      </div>
      <div>
        <router-link to="/services">Services</router-link>
      </div>
      <div>
        <router-link to="/projects">Projects</router-link>
      </div>
      <div>
        <router-link to="/tech">Tech Stack</router-link>
      </div>
      <div>
        <router-link to="/privacy">Privacy Policy</router-link>
      </div>
      <div>
        <router-link to="/imprint">Imprint</router-link>
      </div>
    </div>
    <div class="nav permanent-actions">
      <div>
        <router-link to="/explore">Explore</router-link>
      </div>
      <div>
        <router-link to="/contact">Request</router-link>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
import Vue from "vue";
import Logo from "@/components/Logo.vue";
export default Vue.extend({
  data: function() {
    return {
      displayFlyout: false,
    };
  },
  methods: {
    toggleFlyout: function() {
      this.displayFlyout = !this.displayFlyout;
    },
  },
  components: {
      Logo
  }
});
</script>

<style lang="scss">
@use "../assets/styles/abstracts/abstracts";

.navbar {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  background-color: abstracts.$light;
}

.burger {
  align-self: flex-end;
  color: abstracts.$dark;
}

.permanent-actions {
  display: flex;
  flex-direction: row;
  width: 100%;
  div {
    display: flex;
    color: white;
    align-content: center;
    padding: 1rem;
    width: 50%;
    a {
      width: 100%;
      text-align: center;
      text-decoration: none;
      color: abstracts.$text-light;
    }
  }
  div:nth-child(even) {
    background-color: abstracts.$accent;
  }
  div:nth-child(odd) {
    background-color: abstracts.$accent-dark;
  }
}

.flyout {
  background-color: abstracts.$dark;
  display: flex;
  flex-direction: row;
  flex-wrap: wrap;
  width: 100%;
  opacity: 0;
  visibility: none;
  max-height: 0;
  overflow: hidden;
  transition: opacity 0.35s, visibility 0.01s 0.35s, max-height 0.35s;

  &.is-active {
    opacity: 1;
    visibility: visible;
    transition: opacity 0.35s, visibility 0.01s, max-height 0.35s;
    max-height: 800px;
  }

  div {
    display: flex;
    color: white;
    align-content: center;
    padding: 1rem;
    width: 100%;
    a {
      width: 100%;
      text-align: center;
      text-decoration: none;
      color: abstracts.$text-light;
    }
  }
}
</style>