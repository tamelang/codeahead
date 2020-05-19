<template>
  <div class="home">
    <img src="https://placehold.it/1200x400" />
    <article class="container">
      <h1>About me</h1>
      <p>
        My name is Tim, I work as a software developer, in the area of web
        development, working mainly in the backend and designing software
        architecture and concepts.
      </p>
    </article>
    <article class="container">
      <h1>Projects</h1>
      <p>
        Let me share what I am doing.
      </p>
      <h2>In my day job</h2>
      <p>
        I am working with CMS systems e.g. Adobe Experience Manger (AEM).
        Planning solution to maximise the usage of the out of the box
        functionalities as well as bringing he best user experience for the
        authors and endusers of the website.
      </p>
      <h2>In my free time</h2>
      <p>
        I am working with my friends on a side project called
        <a href="https://bruno.events">"Bruno - Events"</a>.
      </p>
    </article>
  </div>
</template>

<script>
// @ is an alias to /src

export default {
  name: "Home",
  components: {},
};
</script>

<style lang="scss" scoped>
img {
  width: 100%;
}
</style>
