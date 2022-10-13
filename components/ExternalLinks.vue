<template>
  <div
    class="contrainer m-auto w-full fixed flex justify-between items-center text-indigo-600"
  >
    <ul
      class="md:flex items-center pr-10 text-base font-semibold cursor-pointer"
    >
      <li
        v-for="link in Links"
        v-bind:key="link.name"
        class="md:mx-4 md:my-0 my-6"
      >
        <a :href="link.link">{{ link.name }}</a>
      </li>
    </ul>
  </div>
</template>
<script>
import { ref } from 'vue'

export default {
  setup() {
    const open = ref(false)
    const Links = [
      { name: 'HOME', link: '/' },
      { name: 'ABOUT', link: '/About' },
      { name: 'CONTACT', link: '/contact' },
    ]
    return { Links, open }
  },
}
</script>
