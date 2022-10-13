<template>
  <div class="w-full fixed top-0 bg-white z-10 dark:bg-slate-900">
    <div
      class="absolute w-full bg-indigo-200 z-40 inset-0 p-10 h-64 lg:h-64 bg-gradient-to-t from-indigo-200 p-10 space-y-10"
    >
      <div class="overflow-y-auto">
        <ExternalLinks />
      </div>

      <div class="absolute top-0 right-0 pt-6 pr-10">
        <button
          @click="closeMobileMenu"
          class="ml-1 flex items-center justify-center h-10 w-10 rounded-full hover:text-gray-700"
        >
          X
        </button>
      </div>
    </div>
  </div>
</template>

<script>
import ExternalLinks from './ExternalLinks.vue'

export default {
  methods: {
    closeMobileMenu() {
      this.$emit('closeMobileMenu')
    },
  },
  components: { ExternalLinks },
}
</script>
