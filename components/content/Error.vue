<template>
  <div
    class="flex min-h-full flex-col bg-white dark:bg-black pt-40 pb-12"
  >
    <main
      class="mx-auto flex w-full max-w-7xl flex-grow flex-col justify-center px-6 lg:px-8"
    >
      <!-- <div class="flex flex-shrink-0 justify-center">
        <a href="/" class="inline-flex">
          <span class="sr-only">{{ project.$state.name }}</span>
          <img
            :class="[project.$state.logodark ? 'block dark:hidden' : '', '']"
            :src="'/logo/' + project.$state.logoimage"
            :alt="project.$state.name"
            width="120"
            height="120"
          />
          <img
            v-if="project.$state.logodark"
            class="hidden dark:block"
            :src="'/logo/' + project.$state.logodarkimage"
            :alt="project.$state.name"
            width="120"
            height="120"
          />
        </a>
      </div> -->
      <div class="pt-6 pb-16">
        <div class="text-center">
          <p
            class="text-4xl font-semibold dark:text-yellow-400 dark:text-black"
          >
            404
          </p>
          <h1
            class="mt-2 text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl text-yellow-400 dark:text-yellow-400"
          >
            Page not found.
          </h1>
          <p class="mt-2 text-base text-colorTxtLight dark:text-colorTxtDark">
            Sorry, we couldn’t find the page you’re looking for.
          </p>
          <div class="mt-6">
            <NuxtLink
              :to="localePath('/')"
              class="text-base font-medium text-yellow-400 dark:text-yellow-400"
            >
              Go back home
              <span aria-hidden="true"> &rarr;</span>
            </NuxtLink>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>
<script setup>

</script>