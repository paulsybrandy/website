<script setup lang="en">
const route = useRoute()

/**
 * Returns localized GitHub notice string in Turkish/English according to current route.
 * @returns {string}
 */
const getLocalizedNotice = computed((): string => {
  if (route.name?.includes("blog"))
    return "Copyright © 2025, Paul Sybrandy"
  else return "Copyright © 2025, Paul Sybrandy
})
</script>

<template>
  <div
    class="bg-gray-100 text-sm w-full py-4 text-black/50 dark:bg-white/5 dark:text-white/30"
  >
    <div class="responsive-screen">
      <div class="space-y-4 text-center sm:space-y-0 sm:space-x-6 sm:text-left">
        <SmartLink
          href="https://github.com/eggsy/website"
          class="text-center border-b border-transparent hover:border-black/10 dark:hover:border-white/10 transition-colors"
          blank
        >
          {{ getLocalizedNotice }}
        </SmartLink>
      </div>
    </div>
  </div>
</template>
