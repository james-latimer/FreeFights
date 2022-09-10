<template>
  <div class="carousel">
    <vueper-slides  class="no-shadow"
  :visible-slides="3"
  slide-multiple
  :gap="3"
  :slide-ratio="1 / 4"
  :dragging-distance="200"
  :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }">
      <vueper-slide
        v-for="(slide, i) in slides"
        :key="i"
        :image="slide.image"
        :title="slide.title"
        :content="slide.content"
        :video="slide.video" />
    </vueper-slides>
    <button class="btn bg-primary">
      James
    </button>
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'



export default {
  components: {VueperSlides, VueperSlide},
  name: 'HelloWorld',
  data() {
    return {
     slides: [
  {
    video: {
      url: 'https://www.youtube.com/embed/BpfC9-BAUww',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope; picture-in-picture'
      }
    }
  },
  {
  
    video: {
      url: 'https://www.youtube.com/embed/gmDumfShpFI',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope; picture-in-picture'
      },
    }
  },
  {
    video: {
      url: 'https://www.youtube.com/embed/09FkQUh6OJY',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope; picture-in-picture'
      },
    },
  },
  {
    video: {
      url: 'https://www.youtube.com/embed/DpLaqnwFQEY',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope; picture-in-picture'
      }
    }
  },
  {
    video: {
      url: 'https://www.youtube.com/embed/en4hR34Bl8w',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope;'  
      }
    }
  }
]
    }
  }
}
</script>

<style scoped>
  .ex--center-mode {
  width: 600px;
  max-width: 100%;
  margin: auto;
}
.carousel {
  margin: auto;
  padding-top: 5%;
  padding-left: 5%;
  padding-right: 5%;
  width: 75%;
  height: 75;
  background-color: white;
}
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
</style>

