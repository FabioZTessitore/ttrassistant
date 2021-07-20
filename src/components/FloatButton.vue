<template>
  <button class="float-btn" @click="$emit('click')">
    <slot></slot>
  </button>
</template>

<style scoped>
.float-btn {
  position: fixed;
  top: 1rem;
  right: 1rem;
  padding: 1rem 2rem;
  border-radius: 10rem;
  text-transform: uppercase;
  z-index: 1;
  font-size: 2rem;
  line-height: 1;
  background-color: lightpink;
}
</style>