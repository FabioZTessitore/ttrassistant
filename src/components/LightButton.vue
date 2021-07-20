<template>
  <div class="light-btn" :style="{ 'left': left, 'top': top }" :class="{ 'light-btn--on': state }" @click="changeState"></div>
</template>

<script>
export default {
  props: [ 'left', 'top' ],

  data () {
    return {
      state: false
    }
  },

  methods: {
    changeState () {
      this.state = !this.state
    }
  }
}
</script>

<style scoped>
.light-btn {
  position: absolute;
  width: 5rem;
  height: 5rem;
  background-color: transparent;
  border: 3px dashed lightgoldenrodyellow;
  border-radius: 10rem;
  transform: translate(-50%, -50%);
}

@media only screen and (max-width: 800px) {
  .light-btn {
    width: 2.5rem;
    height: 2.5rem;
  }
}

.light-btn--on {
  background-color: lime;
  border: 3px solid limegreen;
}
</style>