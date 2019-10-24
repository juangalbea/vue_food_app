<template>
  <div class="fixed">
    <header>
      <div id="header">
        <div id="logo">
          <img src="../../img/logo.png" alt />
        </div>
        <div id="options">
          <a href="#">Menú completo 9€</a>
          <a href="#">Medio Menú 6€</a>
        </div>
      </div>
    </header>
    <div id="links" class="bottom-shadow">
      <nav>
        <div id="nav">
            <a @click="$emit('select-food', 'Entrantes')" class="hlink" v-bind:class="{ 'foodSelected': food == 'Entrantes' }" href="#">Entrantes</a>
            <a @click="$emit('select-food', 'Sopas')" class="hlink" v-bind:class="{ 'foodSelected': food == 'Sopas' }" href="#">De cuchara</a>
            <a @click="$emit('select-food', 'Principales')" class="hlink" v-bind:class="{ 'foodSelected': food == 'Principales' }" href="#">Principales</a>
            <a @click="$emit('select-food', 'Ensaladas')" class="hlink" v-bind:class="{ 'foodSelected': food == 'Ensaladas' }" href="#">Ensaladas</a>
            <a @click="$emit('select-food', 'Postres')" class="hlink" v-bind:class="{ 'foodSelected': food == 'Postres' }" href="#">Postres</a>
          <img id="burger" src="../../img/burger.png" alt />
        </div>
        <div>
          <span class="step">{{ counter }}</span>
          <img id="cart" src="../../img/cart.png" alt />
        </div>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["counter", "food"],
  data() {
    return {
      title: ''
    }
  },
};
</script>

<style scoped>
.fixed {
  top: 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  position: fixed;
  background: #fff;
  z-index: 2;
}

body {
  display: flex;
  flex-direction: column;
  align-items: center;
}

#logo img {
  width: 10rem;
  margin: 1rem 0;
}

nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 0.9rem 0;
  width: 1200px;
}

#cart {
  width: 2.6rem;
  margin-right: 0.7rem;
  position: relative;
  top: 0.5rem;
}

#links {
  width: 100vw;
  display: flex;
  justify-content: center;
  background: #eee;
}

header {
  width: 1200px;
  margin-bottom: 2rem;
}

header {
  height: 10.2rem;
}

#nav a:hover {
  color: #ea4b7a;
  border: 2px solid #ea4b7a;
}

#options {
  margin-top: 0.9rem;
}

#options a,
foodNoSelected {
  text-decoration: none;
  color: #333;
  background: #eee;
  font-size: 1.2rem;
  font-weight: bold;
  padding: 1.4rem;
  width: 14rem;
  height: 4rem;
  border: 2px solid #eee;
  border-radius: 7px;
  margin-right: 2rem;
}

#nav a {
  text-decoration: none;
  font-size: 0.8rem;
  font-weight: bold;
  font-size: 0.9rem;
  padding: 0.6rem 1rem;
  height: 1.4rem;
  border: 2px solid transparent;
  border-radius: 25px;
  transition: color 0.2s ease;
}

span.step {
  background: #64d1b7;
  border-radius: 0.8em;
  -moz-border-radius: 0.8em;
  -webkit-border-radius: 0.8em;
  color: #ffffff;
  display: inline-block;
  font-weight: bold;
  line-height: 1.6em;
  margin-right: 5px;
  text-align: center;
  width: 1.6em;
  position: relative;
  bottom: 1.6rem;
  left: 3.8rem;
  z-index: 1;
}

.bottom-shadow {
  -moz-box-shadow: 10px 10px 5px #888;
  -webkit-box-shadow: 10px 10px 5px #888;
  box-shadow: 10px 10px 5px #888;
}

#burger {
  width: 2rem;
  display: none;
  margin-left: 10rem;
}

@media only screen and (max-width: 1240px) {
  header,
  #main {
    width: 790px;
  }

  nav {
    width: 790px;
  }
}

@media only screen and (max-width: 820px) {
  header {
    width: 500px;
  }

  nav {
    width: 500px;
  }

  .hlink {
    display: none;
  }

  #burger {
    display: inline;
    margin-left: 2rem;
  }

  #options {
    margin-top: 0.9rem;
  }

  #options a {
    margin-right: 1.5rem;
  }

  nav {
    margin: 0 2rem;
  }
}

.foodSelected {
  color: #ea4b7a;
}
</style>