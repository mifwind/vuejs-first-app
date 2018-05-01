<template>
    <div>
        <h4 v-if="show">Текст, который может стать невидимым</h4>
        <h4 v-else>Текст2</h4>
        <a class="waves-effect waves-light btn" v-on:click="show = !show">Toggle</a>

        <ul>
            <li v-for="(car, i) in cars" :key="i"> {{ i + 1 }} - {{ car.model }} - {{ car.speed }}</li>
        </ul>
    </div>
</template>

<script>
export default {
  name: "less3",
  data() {
    return {
      show: false,
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
