<template>
  <div>
    <div class="row">
      <div class="col s12">
        <app-car></app-car>
      </div>
      <div class="col s12">
        <hr />
      </div>
      <div class="col s12">
        <app-car></app-car>
      </div>
    </div>
   
  </div>
</template>

<script>
import car from "./car/car.vue";

export default {
  name: "less5",
  components: {
    "app-car": car
  }
};
</script>
