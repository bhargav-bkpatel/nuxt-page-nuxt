<template>
  <div class="numbers-card-numbers-card">
    <img :alt="image_alt" :src="image_src" class="numbers-card-image" />
    <span class="numbers-card-number">{{ number }}</span>
    <span class="numbers-card-text">{{ text }}</span>
  </div>
</template>

<script>
export default {
  name: 'NumbersCard',
  props: {
    image_src: {
      type: String,
      default: '/playground_assets/message-200h.png',
    },
    text: {
      type: String,
      default: 'sessions',
    },
    image_alt: {
      type: String,
      default: 'image',
    },
    number: {
      type: String,
      default: '2,148',
    },
  },
}
</script>

<style scoped>
.numbers-card-numbers-card {
  flex: 0 0 auto;
  display: flex;
  align-items: center;
  flex-direction: column;
}
.numbers-card-image {
  width: 45px;
  height: 45px;
  object-fit: cover;
  margin-bottom: var(--dl-space-space-unit);
}
.numbers-card-number {
  color: var(--dl-color-scheme-white);
  font-size: 48px;
  text-align: center;
  line-height: 1.1;
}
.numbers-card-text {
  color: rgba(255, 255, 255, 0.8);
  font-style: normal;
  font-weight: 500;
}
</style>
