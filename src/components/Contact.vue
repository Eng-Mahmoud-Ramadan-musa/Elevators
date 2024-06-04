<template>
   <div class="w-[90%] mt-32 flex-col justify-center items-center mx-auto py-3 mb-5">
    <h2>contact</h2>
  <div class="contact-section w-full flex-col sm:flex-row sm:justify-between sm:items-center justify-center items-center my-7">
    <div class="contact-form"
    data-aos="fade-right"
      data-aos-duration="1000">
      <h3 class="text-2xl text-black">Call Us</h3>
      <form @submit="submitForm">
        <div class="form-group">
          <label for="name">The Name:</label>
          <input type="text" id="name" v-model="name" required>
        </div>
        <div class="form-group">
          <label for="email">E-Mail:</label>
          <input type="email" id="email" v-model="email" required>
        </div>
        <div class="form-group">
          <label for="message">The Message:</label>
          <textarea id="message" v-model="message" required></textarea>
        </div>
        <button type="submit">send</button>
      </form>
    </div>
    <div class="social-media"
    data-aos="fade-left"
      data-aos-duration="1000">
      <h2>Connect With Us On Social Media</h2>
      
      <ul class="mb-5">
        <li><a href="#"><i class="fab fa-facebook-f"></i></a></li>
        <li><a href="#"><i class="fab fa-whatsapp"></i></a></li>
        <li><a href="#"><i class="fab fa-twitter"></i></a></li>
        <li><a href="#"><i class="fab fa-instagram"></i></a></li>
      </ul>
      <a href="#" class="text-2xl"><i class="fa-solid fa-phone mr-2"></i>08437584375</a>
    </div>
  </div>
  </div>
</template>

<script>
export default {
    data() {
    return {
      name: '',
      email: '',
      message: ''
    };
  },
  methods: {
    submitForm() {
      // قم بتنفيذ الإجراءات اللازمة عند إرسال النموذج
      // يمكنك إرسال البيانات إلى الخادم أو تنفيذ أي عمليات أخرى هنا
      console.log('تم إرسال النموذج!');
      console.log('الاسم:', this.name);
      console.log('البريد الإلكتروني:', this.email);
      console.log('الرسالة:', this.message);
    }
  }
}
</script>

<style scoped>
h2 {
  color: #222;
  font-weight: bold;
  font-size: 1.5rem;
  margin-top: 100px;
  margin-bottom: 0
}
.contact-section {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.contact-form {
  flex: 1;
  max-width: 400px;
  padding: 2rem;
  background-color: #cfcece;
  border-radius: 5px;
}

.contact-form h2 {
  text-align: center;
  color: #333;
}

.contact-form form {
  margin-top: 1.5rem;
}

.contact-form .form-group {
  margin-bottom: 1rem;
}

.contact-form label {
  display: block;
  font-weight: bold;
  color: #555;
  margin-bottom: 0.5rem;
}

.contact-form input[type="text"],
.contact-form input[type="email"],
.contact-form textarea {
  width: 100%;
  padding: 0.5rem;
  border: 1px solid #1d1c1c;
  border-radius: 3px;
  background-color: #fff;
  color: #222;
  font-weight: bold;
}

.contact-form button[type="submit"] {
  display: block;
  width: 100%;
  padding: 0.75rem;
  background-color: #fafafa;
  color: #0e0d0d;
  border: none;
  border-radius: 3px;
  cursor: pointer;
  margin-top: 1rem;
}

.contact-form button[type="submit"]:hover {
  background-color: #faf8f8;
}

.social-media {
  flex: 1;
  margin-left: 2rem;
}

.social-media h2 {
  text-align: center;
  color: #333;
}

.social-media ul {
  display: flex;
  justify-content: center;
  list-style: none;
  padding: 0;
  margin-top: 2rem;
}

.social-media ul li {
  margin: 0 0.5rem;
}

.social-media ul li a {
  display: inline-block;
  width: 40px;
  height: 40px;
  line-height: 40px;
  text-align: center;
  font-size: 20px;
  color: #fff;
  background-color: #333;
  border-radius:3px;
}

.social-media ul li a:hover {
  background-color: #555;
}
</style>