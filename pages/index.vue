<!-- eslint-disable vue/multi-word-component-names -->
<template>
  <div class="font-mono">
    <div id="Home"
      class="h-screen lg:h-screen bg-gradient-to-t from-indigo-200 relative overflow-hidden"
    >
      <Nav v-show="!showMobileMenu" @showMobileMenu="showMobileMenu = true"  />
      <MobileMenu
        v-show="showMobileMenu"
        @closeMobileMenu="showMobileMenu = false"
      />

      <!-- images -->
      <img
        class="fixed absolute bottom-0 right-0 lg:left-0 mx-auto h-5/6 object-cover"
        src="images\my_photo_01.png"
        alt="Athiphong"
      />
      <!-- text -->
      <div
        class="hidden lg:flex flex-col absolute top-1/3 left-5 text-xl sm:left-10 sm:text-4xl md:left-1/4 md:text-6xl lg:left-5 xl:left-48 xl:text-7xl font-bold"
      >
        <span class="text-gray-600">Athiphong </span>
        <p id="text" class="text-red-500">Bunkhu</p>
      </div>
      <div
        class="hidden lg:flex flex-col absolute top-1/3 right-5 text-xl sm:right-10 sm:text-4xl md:right-1/4 md:text-6xl lg:right-5 xl:right-48 xl:text-7xl font-bold"
      >
        <span class="text-gray-600">FRONT-END </span>
        <p id="text" class="text-red-500">DEVELOPER</p>
      </div>
    </div>
    <!-- about -->
    <div id="About" class="px-10 dark:bg-slate-900">
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
          <h1 class="text-3xl text-indigo-500 font-bold">SERVICES</h1>
        </div>
        <!-- bottom -->
        <div class="p-5 sm:p-0 flex flex-wrap justify-between">
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">Photography</h1>
            <p class="text-gray-400">
              I'm good at photography.
            </p>
            <a class="text-indigo-600 font-semibold text-sm" href=""
              >Read More</a
            >
          </div>
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">Front end</h1>
            <p class="text-gray-400">
              I can write a web page for you.
            </p>
            <a class="text-indigo-600 font-semibold text-sm" href=""
              >Read More</a
            >
          </div>
          <!-- card -->
          <div
            class="w-full md:w-3/12 shadow-xl rounded-lg p-5 my-3 md:my-10 flex flex-col gap-3"
          >
            <h1 class="font-medium text-lg dark:text-white">UX / UI Design</h1>
            <p class="text-gray-400">
              I can help you design your web page.
            </p>
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
          <h1 class="text-3xl text-indigo-500 font-bold">Works & Projects</h1>
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
    <!-- contact -->
    <div id="contact" class="dark:bg-slate-900">
      <div class="container mx-auto">
        <!-- top -->
        <div class="flex flex-col gap-3 items-center">
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

<script>

export default {
  name: 'IndexPage',
  data() {
    return {
      showMobileMenu: false,
    }
  }
}
</script>
<style>
  html {
  scroll-behavior: smooth;
}
</style>
