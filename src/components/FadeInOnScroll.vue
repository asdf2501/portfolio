<template>
  <div>
    <slot v-if="isActivated" />
    <div ref="element" class="fade-in-on-scroll">
      <slot v-if="!isActivated" />
    </div>
  </div>
</template>

<style>
.fade-in-on-scroll {
  opacity: 0;
}

.fade-in-on-scroll-active {
  opacity: 1;
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-delay: 0s;
  animation-fill-mode: forwards;
}

@keyframes fadeIn {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>

<script>
export default {
  data() {
    return {
      isActivated: false,
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
      const element = this.$refs.element;
      if (!element) {
        return;
      }
      const elementTop = element.getBoundingClientRect().top;
      const windowHeight = window.innerHeight;
      const yOffset = 0;
      if (elementTop - windowHeight + yOffset <= 0) {
        this.isActivated = true;
        window.removeEventListener("scroll", this.handleScroll);
      }
    },
  },
};
</script>