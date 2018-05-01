<template>
  <div id="app">
    
    <app-nav :lessons="lessons" @lessChange="openLess"></app-nav>
    
    <app-less :lesson="currentLesson"></app-less>
  </div>
</template>

<script>
import Navbar from "./components/ui/navbar.vue";
import lessonTemplate from "./components/ui/lessonTemplate.vue";
import lessonsJson from "./assets/data.json";

export default {
  name: "app",
  data() {
    return {
      lessons: lessonsJson,
      currentLesson: lessonsJson[0]
    };
  },
  components: {
    "app-nav": Navbar,
    "app-less": lessonTemplate
  },
  methods: {
    openLess(index) {
      this.currentLesson = this.lessons[index];
    }
  }
};
</script>

<style>

</style>

