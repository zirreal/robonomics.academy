<template>
  <div class="lesson-image" :class="imageClasses">
    
    <figure class="figure clickable-image" v-if="figure" @click="$store.commit('SHOW_IMAGE_POPUP', src)">
      <img :src=pictureSrc.src :alt="alt" />
      <figcaption v-if="figureCaption">{{figureCaption}}</figcaption>
    </figure>

    <g-image v-if="!figure" class="clickable-image" @click="$store.commit('SHOW_IMAGE_POPUP', src)" :src="pictureSrc && pictureSrc" :alt="alt"></g-image>

  </div>
</template>

<script>
export default {

  props: {
    figure: {
      type: Boolean,
      default: false
    },

    src: {
      type: String, 
      required: true
    },

    alt: {
      type: String
    },

    figureCaption: {
      type: String
    },

    imageClasses: {
      type: String,
      default: ''
    }
  },

  computed: {
    pictureSrc() {
      return require(`!!assets-loader!@imagesCourses/${this.src}`)
    }
  }

}
</script>

<style scoped>
  .lesson-image {
    margin-top: var(--gap);
  }

  .lesson-image img {
    display: block;
    margin: 0 auto;
  }

  .lesson-image figcaption {
    margin-top: 10px;
  }

  .mb {
    margin-bottom: var(--gap);
  }

  .full img {
    width: 100%;
  }

  .small {
    width: 60%;
    margin: 0 auto;
  }


</style>