<template>
    <div class="bg-white dark:bg-black py-6">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto flex max-w-2xl flex-col items-end justify-between gap-16 lg:mx-0 lg:max-w-none lg:flex-row">
          <div class="w-full lg:max-w-lg lg:flex-auto">
            <!-- <h2 class="text-3xl font-bold tracking-tight text-gray-900 dark:text-white sm:text-4xl">We’re always looking for awesome people to join us</h2>
            <p class="mt-6 text-xl leading-8 text-gray-900 dark:text-gray-100">Diam nunc lacus lacus aliquam turpis enim. Eget hac velit est euismod lacus. Est non placerat nam arcu. Cras purus nibh cursus sit eu in id.</p> -->
            <img src="https://images.unsplash.com/photo-1606857521015-7f9fcf423740?ixlib=rb-4.0.3&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=1344&h=1104&q=80" alt="" class="mt-16 aspect-[6/5] w-full rounded-2xl bg-gray-50 object-cover lg:aspect-auto lg:h-[34.5rem]" />
          </div>
          <div class="w-full lg:max-w-xl lg:flex-auto mt-12">
            <h3 class="sr-only">Job openings</h3>
            <ul class="-my-8 divide-y divide-gray-100">
              <li v-for="opening in jobOpenings" :key="opening.id" class="py-8">
                <dl class="relative flex flex-wrap gap-x-3">
                  <dt class="sr-only">Role</dt>
                  <dd class="w-full flex-none text-lg font-semibold tracking-tight text-gray-900 dark:text-white">
                    <a :href="opening.href">
                      {{ opening.role }}
                      <span class="absolute inset-0" aria-hidden="true" />
                    </a>
                  </dd>
                  <dt class="sr-only">Description</dt>
                  <dd class="mt-2 w-full flex-none text-base leading-7 text-gray-900 dark:text-gray-100">{{ opening.description }}</dd>
                  <dt class="sr-only">Salary</dt>
                  <dd class="mt-4 text-base font-semibold leading-7 text-gray-900 dark:text-white">{{ opening.salary }}</dd>
                  <dt class="sr-only">Location</dt>
                  <dd class="mt-4 flex items-center gap-x-3 text-base leading-7 text-gray-500">
                    <svg viewBox="0 0 2 2" class="h-0.5 w-0.5 flex-none fill-gray-300" aria-hidden="true">
                      <circle cx="1" cy="1" r="1" />
                    </svg>
                    {{ opening.location }}
                  </dd>
                </dl>
              </li>
            </ul>
            <!-- <div class="mt-8 flex border-t border-gray-100 pt-8">
              <NuxtLink :to="localePath('/article')" class="text-sm font-semibold leading-6 text-yellow-400 hover:text-yellow-500">View all openings <span aria-hidden="true">&rarr;</span></NuxtLink>
            </div> -->
          </div>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  const jobOpenings = [
    {
      id: 1,
      role: 'Chapter 1: The Currency',
      href: '#',
      description:
        'Quos sunt ad dolore ullam qui. Enim et quisquam dicta molestias. Corrupti quo voluptatum eligendi autem labore.',
    },
    {
      id: 2,
      role: 'Chapter 2: The Network',
      href: '#',
      description:
        'Et veniam et officia dolorum rerum. Et voluptas consequatur magni sapiente amet voluptates dolorum. Ut porro aut eveniet.',
    },
    {
      id: 3,
      role: 'Chapter 3: Self-Custody',
      href: '#',
      description:
        'Veniam ipsam nisi quas architecto eos non voluptatem in nemo. Est occaecati nihil omnis delectus illum est.',
    },
    {
      id: 4,
      role: 'Chapter 4: Lightning',
      href: '#',
      description:
        'Veniam ipsam nisi quas architecto eos non voluptatem in nemo. Est occaecati nihil omnis delectus illum est.',
    },
  ]
  </script>