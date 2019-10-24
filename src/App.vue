<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>
export default {
  name: "app",
  components: {}
};
</script>

<style>
/* Base */

* {
  /* font-family: 'Roboto', sans-serif; */
  font-family: "Roboto Condensed", sans-serif;
  color: #777;
}

p {
  font-size: 1.1rem;
}

h3 {
  font-size: 1.4rem;
}

html,
body {
  margin: 0;
  padding: 0;
}

body {
  background: #f5f5f5;
  color: #333;
  font: 14px/1.428571429 "Helvetica Neue", Helvetica, Arial, sans-serif;
  font-weight: 300;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#line {
  position: relative;
  bottom: 1.4rem;
  width: 68rem;
  left: 3rem;
}

main {
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100vw;
  background: #eee;
  position: relative;
  margin-top: 19vh;
  padding-top: 10vh;
  margin-left: 0.2rem;
}

#main {
  width: 1200px;
  margin-bottom: 2rem;
}

@media only screen and (max-width: 1240px) {
  #main {
    width: 790px;
  }

  #line {
    width: 41.5rem;
    left: 3rem;
  }
}

@media only screen and (max-width: 820px) {
  #main {
    width: 500px;
  }

  #line {
    width: 24rem;
    left: 3rem;
  }
}
</style>
