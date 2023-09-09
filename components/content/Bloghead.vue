<template>
    <div class="bg-white dark:bg-black pt-20 sm:pt-24">
      <div class="mx-auto grid max-w-7xl grid-cols-1 gap-x-8 gap-y-12 px-6 sm:gap-y-16 lg:grid-cols-2 lg:px-8">
        <article class="mx-auto w-full max-w-2xl lg:mx-0 lg:max-w-lg">
          <h2 id="featured-post" class="mt-4 text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl">{{ featuredPost.title }}</h2>
          <p class="mt-4 text-lg leading-8 text-gray-900 dark:text-gray-100">{{ featuredPost.description }}</p>
          <div class="mt-4 flex flex-col justify-between gap-6 sm:mt-8 sm:flex-row-reverse sm:gap-8 lg:mt-4 lg:flex-col">
            <div class="flex">
              <NuxtLink :to="localePath(featuredPost.href)" class="text-sm font-semibold leading-6 text-yellow-400" aria-describedby="featured-post">Continue reading <span aria-hidden="true">&rarr;</span></NuxtLink>
            
              
            </div>
            <!-- <div class="flex lg:border-t lg:border-gray-900/10 lg:pt-8">
              <a :href="featuredPost.author.href" class="flex gap-x-2.5 text-sm font-semibold leading-6 text-gray-900 dark:text-white">
                <img :src="featuredPost.author.imageUrl" alt="" class="h-6 w-6 flex-none rounded-full bg-gray-50" />
                {{ featuredPost.author.name }}
              </a>
            </div> -->
          </div>
        </article>
        <div class="mx-auto w-full max-w-2xl border-t border-gray-900/10 pt-12 sm:pt-16 lg:mx-0 lg:max-w-none lg:border-t-0 lg:pt-6">
          <div class="-my-12 divide-y divide-gray-900/10">
            <article v-for="post in posts" :key="post.id" class="py-12">
              <div class="group relative max-w-xl">
                <!-- <time :datetime="post.datetime" class="block text-sm leading-6 text-gray-900 dark:text-gray-100">{{ post.date }}</time> -->
                <h2 class="mt-2 text-lg font-semibold text-gray-900 dark:text-white group-hover:text-gray-900 dark:text-gray-100">
                  <NuxtLink :to="localePath(post.href)">
                    <span class="absolute inset-0" />
                    {{ post.title }}
                </NuxtLink>
                </h2>
                <p class="mt-4 text-sm leading-6 text-gray-900 dark:text-gray-100">{{ post.description }}</p>
              </div>
              <!-- <div class="mt-4 flex">
                <a :href="post.author.href" class="relative flex gap-x-2.5 text-sm font-semibold leading-6 text-gray-900 dark:text-white">
                  <img :src="post.author.imageUrl" alt="" class="h-6 w-6 flex-none rounded-full bg-gray-50" />
                  {{ post.author.name }}
                </a>
              </div> -->
            </article>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const featuredPost = {
    id: 1,
    title: '⚡️ Ride the Lightning ⚡️',
    href: '/guide',
    description:
      'The Lightning Network is not a product or company; it is a set of open standards that define a baseline for interoperability. As such, Lightning node software has been built by a variety of companies and community groups. The vast majority of Lightning software is open source, meaning that the source code is open and licensed in such a way as to enable collaboration, sharing, and community participation in the development process.',
    date: 'Mar 16, 2020',
    datetime: '2020-03-16',
    author: {
      name: 'Michael Foster',
      href: '#',
      imageUrl:
        'https://images.unsplash.com/photo-1519244703995-f4e0f30006d5?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
    },
  }
  const posts = [
    {
      id: 2,
      title: '🇪🇺 Lightning.eu Project Roadmap',
      href: '/roadmap',
      description:
        'We aim to provide guidance and implementation between existing financial structures and the lightning network as it matures. We try to establish these rules and guidance under EU law. We also explore Lightning Network Economies and decentralised value for value models.Here we see a current snapshot of the lightningnetwork provided from the Mempool API & YieldMonitor for currency conversion.',
      date: 'Mar 10, 2020',
      datetime: '2020-03-16',
      author: {
        name: 'Lindsay Walton',
        href: '#',
        imageUrl:
          'https://images.unsplash.com/photo-1517841905240-472988babdf9?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=facearea&facepad=2&w=256&h=256&q=80',
      },
    },
    // More posts...
  ]
  </script>