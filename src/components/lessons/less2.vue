<template>
    <div>
        <div class="input-field">
          <input id="first_name" type="text" v-on:input="value = $event.target.value">
          <label for="first_name">Введите число</label>
        </div>
        
        <p> {{ value }} </p>
        <!-- выводится переменная value -->
        <p> {{ doubleValue }} </p>
        <!-- вызывается метод doubleValue -->
    </div>
</template>

<script>
export default {
  name: "less2",
  data() {
    return {
      value: 1
      //doubleValue: 1,
    };
  },
  methods: {
    increment(value) {
      this.value = value;
      //this.doubleValue = this.value * 2;
    }
  },
  computed: {
    doubleValue() {
      return this.value * 2;
    }
  }
};
</script>
