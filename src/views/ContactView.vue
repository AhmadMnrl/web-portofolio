<template>
  <div class="container mx-auto p-3 md:p-8">
    <div class="flex flex-col-reverse md:flex-row relative">
      <div class="w-full md:w-2/3">
        <div class="flex flex-col gap-4 md:px-20 fade-zoom-up">
          <h1 class="text-2xl md:text-3xl font-bold text-white mb-4">Contact Us</h1>
          <form @submit.prevent="submitForm" class="bg-[#1e1e1f] border-[#383838] rounded-xl text-left text-white p-5 md:py-7 md:px-8">
            <div class="mb-4">
              <label for="name" class="block text-sm text-amber-200 mb-2">Name</label>
              <input type="text" id="name" v-model="form.name" class="w-full px-4 py-2 bg-[#2e2e2f] border border-[#383838] rounded-lg text-white" required>
            </div>
            <div class="mb-4">
              <label for="email" class="block text-sm text-amber-200 mb-2">Email</label>
              <input type="email" id="email" v-model="form.email" class="w-full px-4 py-2 bg-[#2e2e2f] border border-[#383838] rounded-lg text-white" required>
            </div>
            <div class="mb-4">
              <label for="message" class="block text-sm text-amber-200 mb-2">Message</label>
              <textarea id="message" v-model="form.message" class="w-full px-4 py-2 bg-[#2e2e2f] border border-[#383838] rounded-lg text-white" rows="5" required></textarea>
            </div>
            <button type="submit" class="bg-amber-300 text-black px-4 py-2 rounded-lg hover:bg-amber-400">Send Message</button>
          </form>
        </div>
      </div>
      <div class="w-full md:w-1/3 h-fit p-8 md:sticky md:top-24">
        <!-- Sidebar -->
        <div class="flex flex-col text-left">
          <div class="bg-clip-text bg-gradient-to-r from-slate-100 to-amber-300 text-transparent">Let's get in touch!</div>
          <div class="h-[1px] mt-7 mb-7 w-20 bg-amber-200 aos-init aos-animate mr-2"></div>
          <div class="hidden md:block">
            <div class="text-white text-md font-semibold">Other Ways to Reach Us</div>
            <div class="mt-3 flex flex-col gap-1">
              <span class="py-2 px-3 rounded-2xl bg-[#1e1e1f] text-white text-xs cursor-pointer">Email: ahmadmanarulbaehaqi@gmail.com</span>
              <span class="py-2 px-3 rounded-2xl bg-[#1e1e1f] text-white text-xs cursor-pointer">Phone: +62 8571 9127 681</span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      form: {
        name: '',
        email: '',
        message: ''
      }
    }
  },
  methods: {
    submitForm() {
      // Here you can handle the form submission, e.g., send the data to a server
      console.log('Form submitted:', this.form);
      alert('Thank you for contacting us!');
      this.form.name = '';
      this.form.email = '';
      this.form.message = '';
    }
  }
}
</script>

<style scoped>
.paraf {
  -webkit-line-clamp: 3;
  -webkit-box-orient: vertical;
  text-overflow: ellipsis;
  overflow: hidden;
}
@media (min-width: 768px) { 
  .paraf {
    display: -webkit-box;
  }
}
@keyframes fadeZoomUp {
  0% {
    opacity: 0;
    transform: scale(0.5);
  }
  100% {
    opacity: 1;
    transform: scale(1);
  }
}
.fade-zoom-up {
  animation: fadeZoomUp 1s ease-in-out;
  /* animation-delay: 1000ms; */
}
</style>
