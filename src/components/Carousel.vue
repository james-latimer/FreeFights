<template>
  <div class="carousel rounded border border-light">
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
        :video="slide.video" @click="hi()" />
    </vueper-slides>
    
  </div>
</template>

<script>
import { VueperSlides, VueperSlide } from 'vueperslides'
import 'vueperslides/dist/vueperslides.css'



export default {
  components: {VueperSlides, VueperSlide},
  name: 'Carousel',
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
  },{
    video: {
      url: 'https://www.youtube.com/embed/yy2SlIVhBdo',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope;'  
      }
    }
  },{
    video: {
      url: 'https://www.youtube.com/embed/ueryVdb0IfM',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope;'  
      }
    }
  },{
    video: {
      url: 'https://www.youtube.com/embed/24B6AEow9oY',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope;'  
      }
    }
  },{
    video: {
      url: 'https://www.youtube.com/embed/jD-vCU31y00',
      props: {
        allow: 'accelerometer; encrypted-media; gyroscope;'  
      }
    }
  },
]
    }
  },
  methods: {
  hi(){
console.log(3)
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
  padding-top: 2%;
  padding-left: 3%;
  padding-right: 3%;
  width: 75%;
  height: 75;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);

  background-color: #ffffff;
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

