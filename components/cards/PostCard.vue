<template>
  <generic-card
    :title="title"
    :image="image"
    :link="link"
    :image-dimensions="
      $siteConfig.posts.imageDimensions ||
        $siteConfig.cards.imageDimensions ||
        null
    "
  >
    <!-- <span
      v-if="author && $siteConfig.posts.displayAuthor"
      class="author-wrapper"
    >
      <strong>Author:</strong> {{ author }} |
    </span> -->
    <p class="subtitle-wrapper">
      {{ subtitle }}
    </p>
    <span v-if="date" class="date-wrapper">
      <strong>Published on:</strong> {{ datePretty }}
    </span>
  </generic-card>
</template>

<script>
import GenericCard from './GenericCard'
import { getFormattedDate } from '~/helper'
export default {
  components: { GenericCard },
  props: {
    title: {
      type: String,
      default: ''
    },
    image: {
      type: String,
      default: ''
    },
    link: {
      type: String,
      default: ''
    },
    date: {
      type: String,
      default: ''
    },
    subtitle: {
      type: String,
      default: ''
    },
    author: {
      type: String,
      default: ''
    }
  },
  computed: {
    datePretty() {
      return getFormattedDate(this.date)
    }
  }
}
</script>
<style lang="scss">
.subtitle-wrapper {
  font-size: 0.9em;
}
.date-wrapper {
  font-size: 0.8rem;
}
</style>
