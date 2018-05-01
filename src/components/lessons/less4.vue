<template>
  <div>
    <h5>Вызов метода</h5>
    <p>{{ showMess }}</p>

    <h5>Вызов переменной с примененным фильтром</h5>
    <p>{{ message | lowercase }}</p>
    
    <h5>Вызов переменной с примененным двух фильров</h5>
    <p>{{ message | lowercase | capitalize }}</p>
  </div>
</template>

<script>
export default {
  name: "less4",
  data() {
    return {
      message: "Hello world, hello"
    };
  },
  computed: {
    showMess() {
      return this.message.toUpperCase();
    }
  },
  filters: {
    lowercase(value) {
      return value.toLowerCase();
    },
    capitalize(value) {
      if (!value) return "";
      value = value.toString();
      return value.replace(/\b\w/g, function(l) {
        return l.toUpperCase();
      });
    }
  }
};
</script>

