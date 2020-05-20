<template>
  <div id="app">
    <Header>
      <div class="navbar">
        <div class="logo">
          <router-link to="/"
            >code ahead<span class="curser">_</span></router-link
          >
        </div>
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
    </Header>
    <router-view />
  </div>
</template>

<script lang="ts">
import Vue from "vue";
import Header from "@/components/Header.vue";
export default Vue.extend({
  components: {
    Header,
  },
});
</script>
