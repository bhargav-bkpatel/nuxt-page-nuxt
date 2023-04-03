<template>
  <div data-type="slide" class="slide-slide slide" v-bind:class="rootClassName">
    <div class="slide-max-wdith max-content-container">
      <h1 class="slide-text heading2">{{ heading }}</h1>
    </div>
  </div>
</template>

<script>
export default {
  name: 'Slide',
  props: {
    heading: {
      type: String,
      default: 'Slide #1',
    },
    rootClassName: String,
  },
}
</script>

<style scoped>
.slide-slide {
  align-items: center;
  justify-content: center;
}
.slide-max-wdith {
  flex: 0 0 auto;
  display: flex;
  flex-direction: column;
}
.slide-text {
  color: var(--dl-color-scheme-white);
}
.slide-root-class-name {
  background-color: #ff9b1d;
}
.slide-root-class-name1 {
  background-color: #15bd19;
}
.slide-root-class-name2 {
  background-color: var(--dl-color-scheme-pink);
}
.slide-root-class-name3 {
  background-color: var(--dl-color-scheme-lightblue);
}
.slide-root-class-name4 {
  background-color: var(--dl-color-scheme-darkblue);
}
</style>
