<template>
    <div class="bg-white dark:bg-black  sm:pt-0">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <!-- <div class="mx-auto max-w-2xl text-center">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl">From the blog</h2>
          <p class="mt-2 text-lg leading-8 text-gray-900 dark:text-gray-100">Learn how to grow your business with our expert advice.</p>
        </div> -->
        <div class="mx-auto mt-16 grid max-w-2xl grid-cols-1 gap-x-8 gap-y-20 lg:mx-0 lg:max-w-none lg:grid-cols-3">
          <article v-for="post in posts" :key="post.id" class="flex flex-col items-start justify-between">
            <div class="relative w-full">
              <img :src="post.imageUrl" alt="" class="aspect-[16/9] w-full rounded-2xl bg-gray-100 object-cover sm:aspect-[2/1] lg:aspect-[3/2]" />
              <div class="absolute inset-0 rounded-2xl ring-1 ring-inset ring-gray-900/10" />
            </div>
            <div class="max-w-xl">
              <div class="mt-8 flex items-center gap-x-4 text-xs">
                <time :datetime="post.datetime" class="text-gray-500 dark:text-white">{{ post.date }}</time>
                <NuxtLink :to="localePath('/article')" class="relative z-10 rounded-full bg-gray-50 px-3 py-1.5 font-medium text-gray-900 hover:bg-gray-100">{{ post.category.title }}</NuxtLink>
              </div>
              <div class="group relative">
                <h3 class="mt-3 text-lg font-semibold leading-6 text-gray-900 dark:text-white group-hover:text-gray-900 dark:text-gray-100">
                  <NuxtLink :to="localePath(post.href)">
                    <span class="absolute inset-0" />
                    {{ post.title }}
                  </NuxtLink>
                </h3>
                <p class="mt-5 line-clamp-3 text-sm leading-6 text-gray-900 dark:text-gray-100">{{ post.description }}</p>
              </div>
              <!-- <div class="relative mt-8 flex items-center gap-x-4">
                <img :src="post.author.imageUrl" alt="" class="h-10 w-10 rounded-full bg-gray-100" />
                <div class="text-sm leading-6">
                  <p class="font-semibold text-gray-900 dark:text-white">
                    <a :href="post.author.href">
                      <span class="absolute inset-0" />
                      {{ post.author.name }}
                    </a>
                  </p>
                  <p class="text-gray-900 dark:text-gray-100">{{ post.author.role }}</p>
                </div>
              </div> -->
            </div>
          </article>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const posts = [
  
  
    {
      id: 1,
      title: 'Bitcoin',
      href: '/bitcoin',
      description:
        'Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.',
      imageUrl:
        'https://mcdn.wallpapersafari.com/medium/28/14/tsqbrT.jpg',
      date: 'Mar 16, 2020',
      datetime: '2020-03-16',
      category: { title: 'Marketing', href: '#' },
      author: {
        name: 'Michael Foster',
        role: 'Co-Founder / CTO',
        href: '#',
        imageUrl:
          'https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
      },
    },

    {
      id: 1,
      title: 'Satoshi & Lightning',
      href: '/satoshi',
      description:
        'Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.',
      imageUrl:
        'https://public.bnbstatic.com/image/cms/blog/20230727/c562961c-5fbe-4b43-8895-d5846ed48fda',
      date: 'Mar 16, 2020',
      datetime: '2020-03-16',
      category: { title: 'Marketing', href: '#' },
      author: {
        name: 'Michael Foster',
        role: 'Co-Founder / CTO',
        href: '#',
        imageUrl:
          'https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
      },
    },

    {
      id: 1,
      title: 'Stable Coins',
      href: '/stablecoin',
      description:
        'Illo sint voluptas. Error voluptates culpa eligendi. Hic vel totam vitae illo. Non aliquid explicabo necessitatibus unde. Sed exercitationem placeat consectetur nulla deserunt vel. Iusto corrupti dicta.',
      imageUrl:
        'https://zipmex.com/static/64b740628c6dea3f6fe96723aa4b3563/09ff8/stablecoin.png',
      date: 'Mar 16, 2020',
      datetime: '2020-03-16',
      category: { title: 'Marketing', href: '#' },
      author: {
        name: 'Michael Foster',
        role: 'Co-Founder / CTO',
        href: '#',
        imageUrl:
          'https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
      },
    },


    // More posts...
  ]
  </script>