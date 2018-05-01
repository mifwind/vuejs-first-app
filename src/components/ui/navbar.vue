<template>
   <nav>
        <div class="container">
            <div class="nav-wrapper">
                <ul id="nav-mobile" class="left hide-on-med-and-down">
                    <li v-for="(lesson, index) in lessons" :key="index"> 
                      <a 
                        href="javascript:void(0)" 
                        :data-index="index" 
                        @click="openLess"> {{lesson.name}} </a>
                    </li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
export default {
  name: "navbar",
  props: ['lessons'],
  methods: {
    openLess(event) {
      event.preventDefault();
      this.$emit("lessChange", event.target.dataset.index);
    }
  }
};
</script>