<template>
  <div id="app">
    <header>
      <div class="navbar">
        <div class="logo">
          <router-link to="/">Code Ahead</router-link>
        </div>
        <div class="burger">Burger Icon</div>
      </div>
      <ul class="nav flyout">
        <li>
          <router-link to="/about">Services</router-link>
        </li>
        <li>
          <router-link to="/about">Projects</router-link>
        </li>
        <li>
          <router-link to="/about">Technilogies</router-link>
        </li>
        <li>
          <router-link to="/about">People</router-link>
        </li>
        <li>
          <router-link to="/about">Career</router-link>
        </li>
      </ul>
      <ul class="nav permanent-actions">
        <li>
          <router-link to="/projects">Explore</router-link>
        </li>
        <li>
          <router-link to="/contact">Request</router-link>
        </li>
      </ul>
    </header>
    <article>
      <router-view />
    </article>
  </div>
</template>

<style lang="scss">
@use "./assets/styles/abstracts/abstracts";
* {
  margin: 0;
  padding: 0;
}

.navbar {
  width: 100%;
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  //background-color: $secondary;
}

.logo {
  font-size: 54px;
  align-self: flex-start;
  a {
    //color: $primary;
  }
}

.burger {
  align-self: flex-end;
  color: white;
}

.permanent-actions {
  display: flex;
  flex-direction: row;
  list-style-type: none;
  overflow: hidden;
  width: 100%;
  li {
    display: flex;
    color: white;
    align-content: center;
    padding: 1rem;
    width: 50%;
    a {
      width: 100%;
      text-align: center;
      //color: $secondary;
    }
  }
  li:nth-child(even) {
    background-color: $fire-bush;
  }
  li:nth-child(odd) {
    //background-color: $highlight2;
  }
}
.flyout {
  display: block;
  //background-color: $background;
}
</style>
