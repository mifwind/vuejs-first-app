<template>
    <div>
        <p>{{ text }}</p>
        <a class="waves-effect waves-light btn" @click="changeText">Change text</a>

        <p v-bind:class="styleCSS">Цвет: {{ styleCSS }}</p>
        <!-- <input type="text" @input="styleCSS = $event.target.value"> -->

        <div class="row">
          <div class="col s12">
            <div class="picker gray" data-color="gray" @click="showEvent" ></div>
            <div class="picker yellow" data-color="yellow" @click="showEvent"></div>
            <div class="picker pink" data-color="pink" @click="showEvent"></div>
            <div class="picker blue" data-color="blue" @click="showEvent"></div>
          </div>
        </div>
        
    </div>
</template>

<script>
export default {
  name: "less1",
  data() {
    return {
      text: "Этот текст будет изменен",
      changed: false,
      styleCSS: ""
    };
  },
  methods: {
    showEvent(event) {
      this.styleCSS = event.target.dataset.color;
      
    },
    changeText() {
      this.text = this.changed ? "Новый текст" : "Этот текст будет изменен";
      this.changed = !this.changed;
    }
  }
};
</script>

<style scoped>
.picker{
  width: 30px;
  height: 30px;
  border-radius: 50%;
  display: inline-block;
  margin-right: 10px;
  cursor: pointer;
}

.gray {
  background: gray;
}

.yellow {
  background: yellow;
}

.pink {
  background: pink;
}

.blue {
  background: blue;
}
</style>
