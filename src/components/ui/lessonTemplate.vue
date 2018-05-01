<template>
   <div class="container">
      <div class="row">
        <div class="col s12">
          <h1>{{lesson.title}}</h1>
        </div>
      </div>
      <div class="row">
        <div class="col s6">
          <component :is="lesson.tag"></component>
        </div>
        <div class="col s6">
        
          <div v-if="lesson.video.length">
            <div v-for="video in lesson.video" :key="video">
              <iframe width="100%" height="300" :src="video" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe>
            </div>
          </div>
        </div>
      </div>
      
    </div>
</template>

<script>
import less1 from ".././lessons/less1.vue";
import less2 from ".././lessons/less2.vue";
import less3 from ".././lessons/less3.vue";
import less4 from ".././lessons/less4.vue";
import less5 from ".././lessons/less5.vue";
import less6 from ".././lessons/less6.vue";
import less7 from ".././lessons/less7.vue";
import less8 from ".././lessons/less8.vue";

export default {
  name: "lessonTemplate",
  props: ['lesson'],
  components: {
    "app-less1": less1,
    "app-less2": less2,
    "app-less3": less3,
    "app-less4": less4,
    "app-less5": less5,
    "app-less6": less6,
    "app-less7": less7
  },
  data() {
    return {
      
    };
  }
};
</script>