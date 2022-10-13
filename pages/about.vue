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
        <span class="text-5xl text-gray-600 font-bold">ABOUT</span>
      </div>
    </div>
    <!-- about -->
    <div id="#Aboutme" class="px-10">
      <div
        class="container mx-auto py-40 flex flex-col-reverse lg:flex-row items-center gap-20"
      >
        <!-- left -->
        <div class="relative">
          <img
            class="h-1/4 absolute top-0 left-0 -z-10"
            src="images/dots.png"
            alt=""
          />
          <div class="h-full rounded-full overflow-hidden">
            <img class="bg-indigo-300" src="images/my_portrait_03.png" alt="" />
          </div>
        </div>
        <!-- right -->
        <div class="my-auto flex flex-col gap-3">
          <h1 class="text-2xl text-indigo-500 font-bold">ABOUT ME</h1>
          <h1 class="text-3xl font-medium dark:text-white">I'm Fan</h1>
          <p class="text-xl text-gray-400">
            I'm currently studying at King Mongkut's University of Technology
            North Bangkok, Prachinburi Campus. Faculty of Technology and
            Industrial Management Information technology in the field of data
            science.
          </p>
          <h1 class="text-3xl font-medium dark:text-white">My Skills</h1>
          <h2 class="text-xl text-gray-400 font-medium">HTML CSS</h2>
          <h2 class="text-xl text-gray-400 font-medium">Javascript</h2>
          <h2 class="text-xl text-gray-400 font-medium">VueJS</h2>
        </div>
      </div>
    </div>
    <!-- services -->
    <div id="services" class="dark:bg-slate-900">
      <div class="container mx-auto">
        <!-- top -->
        <div class="flex flex-col gap-3 items-center">
          <h1 class="text-indigo-600 font-bold">SERVICES</h1>
          <h1 class="text-3xl dark:text-white">What do I offer?</h1>
        </div>
        <!-- bottom -->
        <div class="p-5 sm:p-0 flex flex-wrap justify-between">
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">Photography</h1>
            <p class="text-gray-400">I'm good at photography.</p>
            <a class="text-indigo-600 font-semibold text-sm" href=""
              >Read More</a
            >
          </div>
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">Front end</h1>
            <p class="text-gray-400">I can write a web page for you.</p>
            <a class="text-indigo-600 font-semibold text-sm" href=""
              >Read More</a
            >
          </div>
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">UX / UI Design</h1>
            <p class="text-gray-400">I can help you design your web page.</p>
            <a class="text-indigo-600 font-semibold text-sm" href=""
              >Read More</a
            >
          </div>
        </div>
      </div>
    </div>
    <!-- works -->
    <div id="works" class="py-40 dark:bg-slate-900">
      <div class="container mx-auto">
        <!-- top -->
        <div class="flex flex-col gap-3 items-center">
          <h1 class="text-indigo-600 font-bold">PORTFOLIO</h1>
          <h1 class="text-3xl dark:text-white">Works & Projects</h1>
        </div>
        <!-- bottom -->
        <div class="p-5 sm:p-0 flex flex-wrap justify-between">
          <!-- card -->
          <div
            class="w-full md:w-5/12 lg:w-1/5 shadow-xl rounded-lg my-3 md:my-10 m-1 transition-all hover:scale-110"
          >
            <img src="/images/working-on-office-icon.png" />
          </div>
          <!-- card -->
          <div
            class="w-full md:w-5/12 lg:w-1/5 shadow-xl rounded-lg my-3 md:my-10 m-1 transition-all hover:scale-110"
          >
            <img src="/images/working-on-office-icon.png" />
          </div>
          <!-- card -->
          <div
            class="w-full md:w-5/12 lg:w-1/5 shadow-xl rounded-lg my-3 md:my-10 m-1 transition-all hover:scale-110"
          >
            <img src="/images/working-on-office-icon.png" />
          </div>
        </div>
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
  name: 'Aboutme',
  components: { Nav, Footer },
  data() {
    return {
      showMobileMenu: false,
    }
  },
}
</script>
