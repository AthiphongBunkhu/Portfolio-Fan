<!-- eslint-disable vue/multi-word-component-names -->
<!-- hidden md:flex space-x-10 text-gray-600 dark:text-gray-100 font-bold text-sm uppercase -->
<template>
  <!-- navbar -->
  <nav class="w-full fixed top-0 bg-white z-10 dark:bg-slate-900">
    <div class="container mx-auto py-5 flex items-center justify-between">
      <h1 class="pl-8 py-4 text-2xl font-bold text-indigo-600">PORTFOLIO</h1>
      <ul
        class="hidden md:flex space-x-10 text-gray-600 dark:text-gray-100 font-bold text-sm uppercase"
      >
        <li
          v-for="link in Links"
          v-bind:key="link.name"
          class="md:mx-4 md:my-0 my-6 text-2xl"
        >
          <a :href="link.link">{{ link.name }}</a>
        </li>
      </ul>
      <!--Ham-->
      <button
        class="md:hidden md:hidden cursor-pointer z-20 "
        @click="showMobileMenu"
      >
        <svg
          class="h-6 w-6"
          xmlns="http://www.w3.org/2000/svg"
          fill="none"
          viewBox="0 0 24 24"
          stroke="currentColor"
        >
          <path
            stroke-linecap="round"
            stroke-linejoin="round"
            stroke-width="2"
            d="M4 6h16M4 12h16M4 18h16"
          />
        </svg>
      </button>
    </div>
  </nav>
</template>
<!-- eslint-disable vue/multi-word-component-names -->
<!-- eslint-disable vue/Use 'const' instead -->

<script>
import { ref } from 'vue'

export default {
  name: 'Nav',
  setup() {
    const open = ref(false)
    const Links = [
      { name: 'Home', link: '/' },
      { name: 'About', link: '/About' },
      { name: 'Contact', link: '/contact' },
    ]
    return { Links, open }
  },
  methods: {
    showMobileMenu() {
      this.$emit('showMobileMenu')
    },
  },
}
</script>
