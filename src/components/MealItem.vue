<template>
    <div class="card">
      <div class="photo">
        <img :src="require(`../img/${meal.image}`)" />
      </div>
      <div class="info">
        <div class="food">
          <p>{{meal.title}}</p>
          <p class="new" v-show="meal.new==true">NUEVO</p>
        </div>
        <div class="price">
          <p>+ {{meal.price}} €</p>
          <button @click="$emit('add-meal', meal.id)" class="plus add pointer">+</button>
        </div>
      </div>
    </div>
</template>

<script>
export default {
  name: "MealItem",
  props: ["meal"],
};
</script>

<style scoped>


.card {
  position: relative;
  margin-bottom: 1.2rem;
  margin-right: 0.7rem;
  margin-left: 0.7rem;
  width: 24rem;
  transition: transform 0.3s;
}

.photo {
  height: 350px;
}

.photo img {
  object-fit: cover;
  width: 24rem;
  height: 100%;
}

.info {
  display: flex;
  flex-direction: column;
  justify-content: space-evenly;
  background: #fff;
  height: 8rem;
}

.price {
  display: flex;
  justify-content: space-between;
}

.info div p,
.info div button {
  margin: 0 2rem;
}

.food {
  display: flex;
  justify-content: space-between;
}

.plus:hover {
  color: #fff;
  background: #64d1b7;
}

.card:hover {
  box-shadow: 10px 10px 20px #ccc;
  transform: translate(0px, -4px);
}

.pointer {
  cursor: pointer;
  outline: none;
  }

.plus {
  color: #64d1b7;
  background: transparent;
  font-size: 1.2rem;
  width: 2rem;
  height: 2rem;
  border: 2px solid #64d1b7;
  border-radius: 50%;
  transition: color 0.2s ease;
  transition: background 0.2s ease;
}

.new {
  display: flex;
  justify-content: center;
  align-items: center;
  position: relative;
  bottom: 35px;
  color: #fff;
  background: #ea4b7a;
  font-size: 0.8rem;
  font-weight: bold;
  width: 4rem;
  height: 1.4rem;
  border: 2px solid #ea4b7a;
  border-radius: 4px;
}

.price p {
  font-size: 1.2rem;
}

@media only screen and (max-width: 820px) {
  .card {
    margin-bottom: 1.2rem;
    width: 26.5rem;
  }

  .photo img {
    object-fit: cover;
    width: 26.5rem;
    height: 100%;
  }
}

</style>