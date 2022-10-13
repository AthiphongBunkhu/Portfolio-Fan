<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="font-mono">
    <div
      class="h-64 lg:h-64 bg-gradient-to-t from-indigo-200 relative overflow-hidden"
    >
      <Nav v-show="!showMobileMenu" @showMobileMenu="showMobileMenu = true"  />
      <MobileMenu
        v-show="showMobileMenu"
        @closeMobileMenu="showMobileMenu = false"
      />
      <!-- text -->
      <div
        class="flex flex-col gap-3 items-center absolute inset-y-1/2 left-1/4 right-1/4"
      >
        <span class="text-5xl text-gray-600 font-bold">CONTACT</span>
      </div>
    </div>
    <!-- contact -->
    <div id="contact" class="py-40">
      <div class="container mx-auto">
        <!-- top -->
        <div class="flex flex-col gap-6 items-center">
          <h1 class="text-3xl text-indigo-600 font-bold">CONTACT ME</h1>
        </div>
        <!-- bottom -->
        <form class="mt-5 p-8 flex flex-col gap-5 items-center">
          <input
            class="p-2 w-full md:w-1/2 ring-1 ring-indigo-300 rounded-sm dark:bg-slate-800 dark:ring-0 dark:text-white"
            type="text"
            placeholder="Name Surname"
          />
          <input
            class="p-2 w-full md:w-1/2 ring-1 ring-indigo-300 rounded-sm dark:bg-slate-800 dark:ring-0 dark:text-white"
            type="email"
            placeholder="Email"
          />
          <textarea
            class="p-2 w-full md:w-1/2 ring-1 ring-indigo-300 rounded-sm dark:bg-slate-800 dark:ring-0 dark:text-white"
            cols="30"
            rows="10"
            placeholder="Message..."
          ></textarea>
          <button
            class="w-1/2 bg-indigo-600 text-white font-medium px-3 py-2 rounded-md cursor-pointer"
          >
            Submit
          </button>
        </form>
      </div>
    </div>
    <Footer />
  </div>
</template>
<!-- eslint-disable vue/multi-word-component-names -->
<script>
import Nav from '../components/Nav.vue'
import Footer from '../components/Footer.vue'

export default {
  name: 'Contact',
  components: { Nav, Footer },
  data() {
    return {
      showMobileMenu: false,
    }
  },
}
</script>
