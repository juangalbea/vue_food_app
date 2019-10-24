<template>
  <div class="container">
    <div v-bind:key="meal.id" v-for="meal in meals" v-show="meal.type==food||food=='Platos'">
      <MealItem v-bind:meal="meal" v-on:add-meal="$emit('add-meal', meal.id)" />
    </div>
  </div>
</template>

<script>
import MealItem from "./MealItem.vue";

export default {
  name: "Meals",
  components: {
    MealItem
  },
  props: ["meals","food"],
};
</script>

<style scoped>

.container {
  display: flex;
  flex-wrap: wrap;
}

@media only screen and (max-width: 820px) {
  .container {
    justify-content: center;
  }
}
</style>