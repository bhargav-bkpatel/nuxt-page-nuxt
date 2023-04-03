<template>
  <div class="event-card-event-card">
    <img :alt="image_alt" :src="image_src" class="event-card-image" />
    <div class="event-card-vertical-line"></div>
    <div class="event-card-container">
      <span class="event-card-title">{{ title }}</span>
      <span class="event-card-text">{{ text }}</span>
    </div>
  </div>
</template>

<script>
export default {
  name: 'EventCard',
  props: {
    title: {
      type: String,
      default: 'Inbound Marketing Secrets',
    },
    image_alt: {
      type: String,
      default: 'image',
    },
    text: {
      type: String,
      default:
        'Amet minim mollit non deserunt ullamco est sit aliqua dolor do amet sint. Velit officia consequat duis enim velit mollit. Exercitation veniam consequat sunt nostrud amet.',
    },
    image_src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixid=Mnw5MTMyMXwwfDF8c2VhcmNofDEwfHxwZW9wbGV8ZW58MHx8fHwxNjQzNzA1NTEx&ixlib=rb-1.2.1&w=200',
    },
  },
}
</script>

<style scoped>
.event-card-event-card {
  width: 100%;
  display: flex;
  grid-gap: 30px;
  padding-top: 30px;
  padding-left: 30px;
  padding-right: 34px;
  padding-bottom: 30px;
  background-color: var(--dl-color-scheme-white);
}
.event-card-image {
  width: 140px;
  height: 140px;
  min-width: 140px;
  object-fit: cover;
  border-radius: var(--dl-radius-radius-round);
}
.event-card-vertical-line {
  width: 1px;
  height: 100%;
  display: flex;
  align-items: flex-start;
  flex-direction: column;
  background-color: rgba(144, 149, 167, 0.2);
}
.event-card-container {
  width: 100%;
  display: flex;
  align-self: stretch;
  align-items: flex-start;
  flex-direction: column;
}
.event-card-title {
  color: var(--dl-color-scheme-darkblue);
  font-size: 18px;
  font-style: normal;
  font-weight: 600;
  margin-bottom: var(--dl-space-space-halfunit);
}
.event-card-text {
  color: var(--dl-color-scheme-darkblue);
  font-size: 14px;
  text-transform: none;
}
@media(max-width: 767px) {
  .event-card-event-card {
    align-items: stretch;
  }
}
@media(max-width: 479px) {
  .event-card-event-card {
    grid-gap: 15px;
    align-items: center;
    flex-direction: column;
  }
  .event-card-vertical-line {
    width: 100%;
    height: 1px;
  }
  .event-card-container {
    align-items: center;
  }
  .event-card-title {
    text-align: center;
  }
  .event-card-text {
    text-align: center;
  }
}
</style>
