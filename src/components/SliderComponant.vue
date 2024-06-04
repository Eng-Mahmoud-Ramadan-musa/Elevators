<template>
  <div class="relative mt-20 h-[400px] overflow-hidden w-full">
    <carousel :autoplay="true">
      <slide v-for="(slide, index) in this.images" :key="index">
      <img :src="currentImage" :key="currentImage" class="slide" :style="{ transform: 'translateX(' + translateX + 'px)' }">
    </slide>
    <button class="absolute top-[50%] left-[3%] bg-inherit hover:bg-gray-400 duration-300 ease-linear text-black font-bold text-3xl p-1 border pt-0 border-gray-500" @click="prevImage"><</button>
    <button class="absolute top-[50%] right-[3%] bg-inherit hover:bg-gray-400 duration-300 ease-linear text-black font-bold text-3xl p-1 border pt-0 border-gray-500" @click="nextImage">></button>
  </carousel>

              </div>
</template>

<script>


export default {
  props: {
    images: {
      type: Array,
      required: true
    }
  },
 data() {
   return{
     currentIndex: 0,
      translateX: 0,
      intervalId: null
    };
  },
  computed: {
    currentImage() {
      return this.images[this.currentIndex];
    }
  },
  mounted() {
    
    setInterval(() => {this.startInterval();}, 5000);
      
  },
  methods: {
    startInterval() {
      this.intervalId = setInterval(() => {
        this.nextImage();
      }, 1000);
    },
    stopInterval() {
      clearInterval(this.intervalId);
    },
    prevImage() {
      this.stopInterval();
      if (this.currentIndex === 0) {
        this.currentIndex = this.images.length - 1;
      } else {
        this.currentIndex--;
      }
      this.translateX = -this.$refs.carousel.offsetWidth;
      this.$nextTick(() => {
        this.translateX = 0;
        this.startInterval();
      });
    },
    nextImage() {
      this.stopInterval();
      if (this.currentIndex === this.images.length - 1) {
        this.currentIndex = 0;
      } else {
        this.currentIndex++;
      }
      this.translateX = this.$refs.carousel.offsetWidth;
      this.$nextTick(() => {
        this.translateX = 0;
        this.startInterval();
      });
    }
  }
}
</script>

<style>
.carousel {
  position: relative;
  scroll-snap-type: x mandatory;
  -webkit-overflow-scrolling: touch;
  width: 100%;
  height: 100%;
}

.slide {
  width: 100%;
  height: 100%;
  transition: transform 0.5s ;
}

.slide-enter-active,
.slide-leave-active {
  transition: transform 0.5s;
}

.slide-enter,
.slide-leave-to {
  transform: translateX(0);
}

</style>