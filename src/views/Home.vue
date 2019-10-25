<template>
  <div id="app">
    <Header v-bind:counter="counter" v-bind:food="food" v-on:select-food="selectFood" />
    <main>
      <div id="main">
        <div id="entrantes">
          <h3>{{this.food}}</h3>
          <hr id="line" />
        </div>
        <Meals v-bind:meals="meals" v-bind:food="food" v-on:add-meal="addMeal" />
      </div>
    </main>
  </div>
</template>
  props: ["counter", "food"],
<script>
import Header from "../components/layout/Header";
import Meals from "../components/Meals";

export default {
  name: "Home",
  components: {
    Header,
    Meals
  },
  data() {
    return {
      counter: 0,
      food: "Platos",
      meals: [
        {
          id: 1,
          title: "Berries",
          image: "berries.jpg",
          price: "3,50",
          type: "Postres",
          added: true,
          new: true
        },
        {
          id: 2,
          title: "Bibimbap",
          image: "bibimbap.jpg",
          price: "7,50",
          type: "Principales",
          added: true,
          new: false
        },
        {
          id: 3,
          title: "Biryani",
          image: "biryani.jpg",
          price: "6,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 4,
          title: "Burger",
          image: "burger.jpg",
          price: "6,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 5,
          title: "Caprese Salad",
          image: "caprese.jpg",
          price: "5,50",
          type: "Ensaladas",
          added: true,
          new: true
        },
        {
          id: 6,
          title: "Cereals",
          image: "cereals.jpg",
          price: "4,50",
          type: "Postres",
          added: true,
          new: false
        },
        {
          id: 7,
          title: "Falafel",
          image: "falafel.jpg",
          price: "6,50",
          type: "Entrantes",
          added: true,
          new: true
        },
        {
          id: 8,
          title: "Catalan Cream",
          image: "catalan-cream.jpg",
          price: "3,50",
          type: "Postres",
          added: true,
          new: false
        },
        {
          id: 9,
          title: "Platter",
          image: "platter.jpg",
          price: "7,50",
          type: "Entrantes",
          added: true,
          new: false
        },
        {
          id: 10,
          title: "Spicy soup",
          image: "spicy-soup.jpg",
          price: "4,50",
          type: "Sopas",
          added: true,
          new: false
        },
        {
          id: 11,
          title: "Borscht",
          image: "borscht.jpg",
          price: "4,50",
          type: "Sopas",
          added: true,
          new: true
        },
        {
          id: 12,
          title: "Italian burguer",
          image: "italian-burger.jpg",
          price: "7,50",
          type: "Principales",
          added: true,
          new: false
        },
        {
          id: 13,
          title: "Lasagna",
          image: "lasagna.jpg",
          price: "6,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 14,
          title: "Macaroons",
          image: "macaroons.jpg",
          price: "4,50",
          type: "Postres",
          added: true,
          new: true
        },
        {
          id: 15,
          title: "Noodle soup",
          image: "noodle-soup.jpg",
          price: "5,50",
          type: "Sopas",
          added: true,
          new: true
        },
        {
          id: 16,
          title: "Pad thai",
          image: "pad-thai.jpg",
          price: "7,50",
          type: "Principales",
          added: true,
          new: false
        },
        {
          id: 17,
          title: "Paella",
          image: "paella.jpg",
          price: "6,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 18,
          title: "Pakcake",
          image: "pancake.jpg",
          price: "3,50",
          type: "Postres",
          added: true,
          new: false
        },
        {
          id: 19,
          title: "Panzanella",
          image: "panzanella.jpg",
          price: "5,50",
          type: "Ensaladas",
          added: true,
          new: false
        },
        {
          id: 20,
          title: "Pasta pesto",
          image: "pasta-pesto.jpg",
          price: "4,50",
          type: "Principales",
          added: true,
          new: false
        },
        {
          id: 21,
          title: "Pepper olives pizza",
          image: "pepper-olive-pizza.jpg",
          price: "5,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 22,
          title: "Pizza Napolitana",
          image: "pizza-napolitana.jpg",
          price: "5,50",
          type: "Principales",
          added: true,
          new: false
        },
        {
          id: 23,
          title: "Pomegranate",
          image: "pomegranate.jpg",
          price: "2,50",
          type: "Postres",
          added: true,
          new: true
        },
        {
          id: 24,
          title: "Prawns",
          image: "prawn.jpg",
          price: "6,50",
          type: "Entrantes",
          added: true,
          new: true
        },
        {
          id: 25,
          title: "Raspberry",
          image: "raspberry.jpg",
          price: "3,50",
          type: "Postres",
          added: true,
          new: true
        },
        {
          id: 26,
          title: "Mix salad leaf",
          image: "salad-leaf.jpg",
          price: "4,50",
          type: "Ensaladas",
          added: true,
          new: false
        },
        {
          id: 27,
          title: "Salmon",
          image: "salmon.jpg",
          price: "6,50",
          type: "Principales",
          added: true,
          new: true
        },
        {
          id: 28,
          title: "Scampi",
          image: "scampi.jpg",
          price: "5,50",
          type: "Entrantes",
          added: true,
          new: false
        },
        {
          id: 29,
          title: "Thai salad",
          image: "thai-salad.jpg",
          price: "5,50",
          type: "Ensaladas",
          added: true,
          new: false
        },
        {
          id: 30,
          title: "Viet soup",
          image: "viet-soup.jpg",
          price: "4,50",
          type: "Sopas",
          added: true,
          new: false
        }
      ]
    };
  },
  methods: {
    addMeal() {
      this.counter += 1;
    },
    selectFood(newFood) {
      this.food = newFood;
    }
  }
};
</script>

<style>
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
  margin-top: 11rem;
  padding-top: 10vh;
  margin-left: 0.2rem;
}

#main {
  width: 1220px;
  margin-bottom: 2rem;
}

#entrantes {
  margin: 0 0.6rem;
}

@media only screen and (max-width: 1240px) {
  #main {
    width: 820px;
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
