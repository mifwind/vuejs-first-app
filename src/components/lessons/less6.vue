<template>
  <div>
    <div class="row">
      <div class="col s12">
        <app-car v-for="(car, i) in cars" :key="i" :index="i" :car="car"></app-car>
      </div>
    </div>
   
  </div>
</template>

<script>
import car from "./car/car2.vue";

export default {
  name: "less5",
  data() {
    return {
      cars: [
        { model: "BMW", speed: 250 },
        { model: "Audi", speed: 240 },
        { model: "Mersedes-Benz AMG", speed: 350 },
        { model: "Ford", speed: 160 },
        { model: "Volvo", speed: 160 },
        { model: "Siat", speed: 160 },
        { model: "Fiat", speed: 160 }
      ]
    };
  },
  components: {
    "app-car": car
  }
};
</script>
