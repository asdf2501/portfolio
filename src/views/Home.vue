<template>
  <div class="container">
    <div class="fade-in-on-scroll" v-show="isVisible">
      <h1>Hello World!</h1>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      isVisible: false
    };
  },
  mounted() {
    window.addEventListener("scroll", this.handleScroll);
  },
  destroyed() {
    window.removeEventListener("scroll", this.handleScroll);
  },
  methods: {
    handleScroll() {
      const element = this.$el;
      const elementTop = element.getBoundingClientRect().top;
      const windowHeight = window.innerHeight;
      if (elementTop < windowHeight) {
        this.isVisible = true;
        window.removeEventListener("scroll", this.handleScroll);
      }
    }
  }
};
</script>

<style>
.container {
  height: 200vh;
}

.fade-in-on-scroll {
  opacity: 0;
  transition: opacity 0.5s ease-in-out;
}

.fade-in-on-scroll.v-show-enter-active,
.fade-in-on-scroll.v-show-leave-active {
  transition: opacity 0.5s ease-in-out;
}

.fade-in-on-scroll.v-show-enter,
.fade-in-on-scroll.v-show-leave-to {
  opacity: 0;
}
</style>