<template>
  <header class="flex justify-between px-[10%] py-1 items-center bg-slate-900 fixed top-0 left-0 w-full z-50 pt-3">
    <a href="#" class="w-[50px] h-[50px] border rounded-full overflow-hidden"
      ><img class="w-full h-full object-cover" :src="img" alt=""
    /></a>
    <nav class="hidden sm:flex gap-3 text-2xl font-bold">
      <a href="#aniwiae almasaeid" class="text-white">aniwiae almasaeid</a>
      <a href="#userOpinions" class="text-white">customer opinions</a>
      <a href="#contact" class="text-white">contact us</a>
    </nav>
    <i class="fa-solid fa-bars sm:hidden mr-9" @click="showMenu = !showMenu"></i>
    <ul v-if="showMenu" class="absolute top-14 p-3 rounded-lg right-14 gap-3 text-2xl font-bold sm:hidden bg-gray-800">
      <li @click="showMenu = !showMenu"><a href="#aniwiae almasaeid" class="text-white block mt-2 border-b pb-1">aniwiae almasaeid</a></li>
      <li @click="showMenu = !showMenu"><a href="#userOpinions" class="text-white block mt-2 border-b pb-1">customer opinions</a></li>
      <li @click="showMenu = !showMenu"><a href="#contact" class="text-white mt-3">contact us</a></li>
    </ul>
  </header>
  <section
    class="relative w-[90%] mt-4 h-[75vh] flex-col gap-x-12 justify-center mx-auto py-3"
  >
  <div class="absolute top-[20%] right-[5%] text-2xl flex gap-3 z-40">
        <span><a href="https://www.facebook.com/profile.php?id=100007283614477"><i class="fab fa-facebook-f fa-fade text-white bg-blue-700 rounded-full w-8 h-8 py-1"></i></a></span>
        <span><a href="https://wa.me/+201129780862"><i class="fab fa-whatsapp fa-fade text-white rounded-full w-8 h-8 py-1 bg-green-500"></i></a></span>
        <span><a href="https://t.me/MahmoudRamadan11"><i class="fa-brands fa-telegram fa-fade text-white  bg-blue-500 rounded-full w-8 h-8 py-1"></i></a></span>
      </div>
      <button class="absolute top-[80%] left-[15%] z-40 bg-gray-500 rounded-lg text-2xl font-bold px-2 py-1 hover:bg-gray-700 transition-colors duration-300">about</button>
  <slider-componant :images="this.image" />
  </section>
  <section id="aniwiae almasaeid"
    class="relative w-[90%] mt-24 flex-col justify-center mx-auto py-3"
  >
  <h2>aniwiae almasaeid</h2>
<div  class=" flex-col justify-center w-[90%]">
  <div
      class="w-full sm:h-[400px] relative overflow-hidden mx-auto sm:flex justify-between items-end mt-5"
    >
    <slider-componant :images="this.image1" data-aos="fade-right"
      data-aos-duration="1000" />

      <p class="w-full pb-16 pStyle mt-4"
      data-aos="fade-left"
      data-aos-duration="1000">
      <span class="as">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti amet
        iure dicta perspiciatis dolore ipsa aut tempora iste nesciunt similique.
      </span>
      </p>
    </div>
  <div id="secound"
      class="w-full sm:h-[400px] relative overflow-hidden mx-auto sm:flex-row-reverse justify-between items-end mt-5"
    >
  <slider-componant :images="this.image2"
 data-aos="fade-left"
      data-aos-duration="1000" />

      <p class="w-full pb-16 pStyle mt-4"
      data-aos="fade-right"
      data-aos-duration="1000">
      <span class="as">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti amet
        iure dicta perspiciatis dolore ipsa aut tempora iste nesciunt similique.
      </span>
      </p>
    </div>
    <div
      class="w-full sm:h-[400px] relative overflow-hidden mx-auto sm:flex justify-between items-end mt-5"
    >
  <slider-componant :images="this.image3"
       data-aos="fade-right"
      data-aos-duration="1000" />

      <p class="w-full pb-16 pStyle mt-4"
      data-aos="fade-left"
      data-aos-duration="1000">
      <span class="as">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Deleniti amet
        iure dicta perspiciatis dolore ipsa aut tempora iste nesciunt similique.
      </span>
      </p>
    </div>
</div>
  </section>
  <section id="userOpinions"
    class="w-[90%] mt-24 flex-col justify-center mx-auto py-3"
  >
  <h2>userOpinions</h2>
<rating />
  </section>
<contact id="contact" />
  <footer class="w-full fixed bottom-0 left-0 px-[10%] py-2 sm:flex sm:justify-between items-center justify-center mt-16 bg-slate-900"><p class="text-2xl text-white text-nowrap">design by &copy; <span class="font-bold text-red-600">mahmoud ramadan</span></p>    
  <div class="text-xl flex gap-3 justify-center sm:justify-end w-full">
        <span><a href="https://www.facebook.com/profile.php?id=100007283614477"><i class="fab fa-facebook-f fa-fade text-white bg-blue-700 rounded-full w-7 h-7 py-1"></i></a></span>
        <span><a href="https://wa.me/+201129780862"><i class="fab fa-whatsapp fa-fade text-white rounded-full w-7 h-7 py-1 bg-green-500"></i></a></span>
        <span><a href="https://t.me/MahmoudRamadan11"><i class="fa-brands fa-telegram fa-fade text-white  bg-blue-500 rounded-full w-7 h-87 py-1"></i></a></span>
      </div>
      </footer>
</template>

<script>
import SliderComponant from './components/SliderComponant.vue';
import Contact from "./components/Contact.vue";
import AOS from 'aos';
import 'aos/dist/aos.css';
import Rating from './components/Rating.vue';
import img from "./assets/images/432330133_122110386440233717_4916679324521121524_n.jpg";
import img1 from "./assets/images/js.png";
import img2 from "./assets/images/images (1).jpeg";
import img3 from "./assets/images/images (2).jpeg";
import img4 from "./assets/images/images.jpeg";
import img5 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.37_c7d8294a.jpg";
import img6 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.37_f9bdda1e.jpg";
import img7 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.38_1902f4a7.jpg";
import img8 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.38_ba3f6844.jpg";
import img9 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.39_97423d10.jpg";
import img10 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.39_c7d89ef3.jpg";
import img11 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.39_fc4c5a52.jpg";
import img12 from "./assets/images/WhatsApp Image 2024-06-03 at 19.10.39_ffa82818.jpg";
import img13 from "./assets/images/2200-202104131633591186.jpg";
import img14 from "./assets/images/download (2).jpeg";
import img15 from "./assets/images/images (4).jpeg";


export default {
  data() {
    return {
      img: img,
     image: [img, img13, img14, img15],
     image1: [img6, img7, img8,img9],
     image2: [img1,img2, img3, img4,img12],
     image3: [img5, img10, img11],
      showMenu: false,
    };
  },
  components: { SliderComponant,Rating ,Contact },
  mounted() {
    AOS.init();
  },
};
</script>
<style scoped>
.pStyle {
color:#222;
font-size: 20px;
text-align: left;
padding-inline: 20px;
}
h2 {
  color: #222;
  font-weight: bold;
  font-size: 1.5rem;
  margin-top: 100px;
  margin-bottom: 0
}
.truncate {
  @apply overflow-hidden whitespace-nowrap text-ellipsis;
}
@media (min-width: 640px) {
  #secound {
  display: flex;
  flex-direction: row-reverse;
}
}

</style>
