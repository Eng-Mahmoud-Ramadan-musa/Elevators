<template>

  <!-- **************** -->
  <div class="w-full sm:flex justify-between items-center mt-5">
  <div
  v-for="user in this.users" :key="user.id"
    data-aos="fade-up"
      data-aos-duration="1000"
      class="w-[300px] h-[90%] p-3 relative overflow-hidden mx-auto flex-col border border-black rounded-lg m-2"
    >
      <div
        class="w-full relative overflow-hidden flex justify-center items-center mb-2"
      >
        <div class="w-[100px] h-[100px] rounded-full overflow-hidden">
          <img class="w-full h-full object-cover" :src="user.img" alt="" />
        </div>
      </div>
      <div class="flex-col w-full">
        <h3 class="text-2xl font-bold mb-2 text-blue-700">{{ user.name }}</h3>
        <p class="truncate pStyle">
          {{ user.massge }}
        </p>
        <div class="rating">
    <div class="star-rating">
      <span v-for="star in 5" :key="star" :class="{filled: star <= user.rat}">
        ★
      </span>
    </div>
    <p class="rating-text">تقييم المستخدم: {{ user.rat }}</p>
  </div>
      </div>
    </div>

</div>
</template>

<script>
import ima1 from "../assets/images/download (1).jpeg";
import ima2 from "../assets/images/download.jpeg";
import ima3 from "../assets/images/images (3).jpeg";
export default {
    data() {
    return {
      rating: 4,
      currentRating: 0,
      users:[
        {id:1, name: "fhdjf",massge: "fskdhfsd dffjs sfdhfjsdjkf skdfhjd sdjfk fjdks sdkjflsk" ,img: ima1, rat: 4}
        ,{id:2, name: "dhfj",massge: "fskdhfsd dffjs sfdhfjsdjkf skdfhjd sdjfk fjdks sdkjflsk" ,img: ima2, rat: 3}
        ,{id:3, name: "cmxv",massge: "fskdhfsd dffjs sfdhfjsdjkf skdfhjd sdjfk fjdks sdkjflsk" ,img: ima3, rat: 5}
      ] 
    };
  },
  methods: {
    setRating(star) {
      this.currentRating = star;
    }
  }
}
</script>

<style>
    .rating {
      width: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 10px;
}
.pStyle {
color:#222;
font-size: 20px;
text-align: center;
padding-inline: 20px;
}
.star-rating {
        color: #9b9b98; /* تغيير لون النجوم إلى الذهبي */
        font-size: 24px;
}

.star-rating .filled {
        color: #ffd700; /* تغيير لون النجوم الممتلئة */
      }

.rating-text {
  font-weight: bold;
  margin-top: 10px;
  color: #222;
}
</style>