<template>
  <div>
    <div class="col s12 m6">
      <div class="card">
        <div class="card-content">
          <span class="card-title">{{ car.model }}</span>
          <p>{{ index + 1 }} - {{ car.speed }}</p>
          <!--  -  -->
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "car2",
  props: ['index','car']
};
</script>

