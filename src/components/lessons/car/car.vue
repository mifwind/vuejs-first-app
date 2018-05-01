<template>
  <div>
    <div class="col s12 m6" v-for="(car, i) in cars" :key="i">
      <div class="card">
        <div class="card-content">
          <span class="card-title">{{ car.model }}</span>
          <p>{{ i + 1 }} - {{ car.speed }}</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "car",
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
  }
};
</script>

