<template>
  <div class="speaker-card-speaker-card">
    <div class="speaker-card-image-container">
      <img :alt="image_alt" :src="image_src" class="speaker-card-image" />
      <div class="speaker-card-read-more-container">
        <span class="speaker-card-hint">read more</span>
        <svg viewBox="0 0 1024 1024" class="speaker-card-icon">
          <path
            d="M621.254 877.254l320-320c24.994-24.992 24.994-65.516 0-90.51l-320-320c-24.994-24.992-65.516-24.992-90.51 0-24.994 24.994-24.994 65.516 0 90.51l210.746 210.746h-613.49c-35.346 0-64 28.654-64 64s28.654 64 64 64h613.49l-210.746 210.746c-12.496 12.496-18.744 28.876-18.744 45.254s6.248 32.758 18.744 45.254c24.994 24.994 65.516 24.994 90.51 0z"
          ></path>
        </svg>
      </div>
    </div>
    <span class="speaker-card-first-name">{{ firstName }}</span>
    <span class="speaker-card-last-name">{{ lastName }}</span>
    <span class="speaker-card-text">{{ role }}</span>
  </div>
</template>

<script>
export default {
  name: 'SpeakerCard',
  props: {
    firstName: {
      type: String,
      default: 'Jonathan',
    },
    lastName: {
      type: String,
      default: 'carey',
    },
    image_alt: {
      type: String,
      default: 'image',
    },
    role: {
      type: String,
      default: 'brand manager @ pepsi',
    },
    image_src: {
      type: String,
      default:
        'https://images.unsplash.com/photo-1507003211169-0a1dd7228f2d?ixid=Mnw5MTMyMXwwfDF8c2VhcmNofDEwfHxwZW9wbGV8ZW58MHx8fHwxNjQzNzA1NTEx&ixlib=rb-1.2.1&w=300',
    },
  },
}
</script>

<style scoped>
.speaker-card-speaker-card {
  display: flex;
  position: relative;
  align-items: flex-start;
  flex-direction: column;
}
.speaker-card-image-container {
  width: 100%;
  height: 100%;
  display: flex;
  position: relative;
  min-width: 255px;
  min-height: 255px;
  align-items: flex-end;
  margin-bottom: var(--dl-space-space-unit);
  flex-direction: column;
  justify-content: flex-end;
}
.speaker-card-image {
  left: 0px;
  width: 100%;
  bottom: 0px;
  filter: grayscale();
  height: 100%;
  position: absolute;
  object-fit: cover;
}
.speaker-card-read-more-container {
  flex: 1;
  width: 100%;
  cursor: pointer;
  display: flex;
  opacity: 0;
  z-index: 1;
  transition: 0.3s;
  align-items: flex-end;
  padding-right: 20px;
  flex-direction: row;
  padding-bottom: 18px;
  justify-content: flex-end;
  background-color: rgba(251, 39, 90, 0.6);
}
.speaker-card-read-more-container:hover {
  opacity: 1;
}
.speaker-card-hint {
  color: var(--dl-color-scheme-white);
  font-style: normal;
  font-weight: 600;
  line-height: 1.3;
  margin-right: 11px;
}
.speaker-card-icon {
  fill: var(--dl-color-scheme-white);
  width: 21px;
  height: 21px;
}
.speaker-card-first-name {
  font-size: 30px;
  font-style: normal;
  font-weight: 700;
  line-height: 1.1;
}
.speaker-card-last-name {
  color: var(--dl-color-scheme-lightblue);
  font-size: 30px;
  font-style: normal;
  font-weight: 700;
  line-height: 1.1;
  margin-bottom: var(--dl-space-space-halfunit);
}
.speaker-card-text {
  font-size: 14px;
  font-style: normal;
  font-weight: 500;
}
</style>
