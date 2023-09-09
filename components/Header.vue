<script setup>
import { ref } from "vue";
import {
  Dialog,
  DialogPanel,
  Disclosure,
  DisclosureButton,
  DisclosurePanel,
  Popover,
  PopoverButton,
  PopoverGroup,
  PopoverPanel,
  Menu, 
  MenuButton, 
  MenuItem, 
  MenuItems
} from "@headlessui/vue";
import { BitcoinCircleIcon, ExchangeIcon, LightningIcon, CoinsIcon, SatoshiV3Icon, SafeIcon } from '@bitcoin-design/bitcoin-icons-vue/outline';
import {
  ArrowPathIcon,
  Bars3Icon,
  BellIcon,
  ChartPieIcon,
  CursorArrowRaysIcon,
  FingerPrintIcon,
  SquaresPlusIcon,
  XMarkIcon,
  WalletIcon,
  ServerStackIcon,
  RocketLaunchIcon
} from "@heroicons/vue/24/outline";
import {
  ChevronDownIcon,
  PhoneIcon,
  PlayCircleIcon,
} from "@heroicons/vue/20/solid";

const mobileMenuOpen = ref(false);


const products = [

{ name: 'Lightning', description: 'Rent your own Bitcoin or Lightning Node', href: '/guide', icon: LightningIcon },
  { name: 'Wallets', description: 'The easiest way to start with lightning', href: '/wallets', icon: WalletIcon },
  { name: 'Currency', description: 'Stacking Sats, best way to bitcoin', href: '/currency', icon: SafeIcon },

  // { name: 'Invest', description: 'Invest in Lightning.eu ', href: '#', icon: RocketLaunchIcon },
]


const transfers = [

{ name: 'Bitcoin', description: 'Layer 2 transfers', href: '/bitcoin', icon: BitcoinCircleIcon },
  { name: 'Satoshis', description: 'The atomic unit of the lightning network', href: '/satoshi', icon: SatoshiV3Icon },
  { name: 'Stable Coins', description: 'Transfer USDt', href: '/stablecoin', icon: CoinsIcon },
  // { name: 'Invest', description: 'Invest in Lightning.eu ', href: '#', icon: RocketLaunchIcon },
]


const development = [
{ name: 'Merchants', href: '#', description: 'Solutions for merchants to integrate payments' },
  { name: 'Resources', href: '#', description: 'Dictionary abreviations and lightning words, Links to LND, BND, Bitcoin Design' },
  // {
  //   name: 'Support',
  //   href: '#',
  //   description: 'Get in touch with our dedicated support team or reach out on our community forums',
  // },
  // { name: 'Blog', href: '#', description: 'Read our latest announcements and get perspectives from our team' },
]


const company = [


  { name: 'Worldmap', href: '#', description: 'Visualise the european lightning network' },
  { name: 'Transaction Lookup', href: '#', description: 'Lookup Tranasctions by ID or wallet' },
  // {
  //   name: 'Support',
  //   href: '#',
  //   description: 'Get in touch with our dedicated support team or reach out on our community forums',
  // },
  // { name: 'Blog', href: '#', description: 'Read our latest announcements and get perspectives from our team' },
]


// SPLICED AUTH


</script>

<template>
  <header class="bg-colorBgLight dark:bg-colorBgDark backdrop-blur-sm fixed w-full z-50">
    <nav
      class="mx-auto flex max-w-7xl items-center justify-between p-3 lg:px-8 "
      aria-label="Global"
    >
      <div class="flex lg:flex-1">
        <NuxtLink to="/" class="-m-1.5 p-1.5">
          <span class="sr-only">Codex.eu.com</span>
          <img
            class="h-12 w-auto hidden dark:block"
            src="/logo-bright.png"
            alt=""
          />

          <img
            class="h-12 w-auto dark:hidden block"
            src="/logo-light.png"
            alt=""
          />


        </NuxtLink>
      </div>
      <div class="flex lg:hidden border-2 rounded-md border-yellow-400 dark:border-white p-1">
        <button
          type="button"
          class="-m-2.5 inline-flex items-center justify-center rounded-md p-2.5 text-white dark:text-black"
          @click="mobileMenuOpen = true"
        >
          <span class="sr-only">Open main menu</span>
          <Bars3Icon class="h-6 w-6" aria-hidden="true" />
        </button>
      </div>
      <PopoverGroup class="hidden lg:flex lg:gap-x-12">





          <NuxtLink :to="localePath('/')"
            class="text-sm font-semibold leading-6 text-yellow-400 dark:text-black"
            
          >
            Home
          </NuxtLink>


          <Popover class="relative">
          <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-yellow-400 dark:text-black">
            Guides
            <ChevronDownIcon class="h-5 w-5 flex-none text-yellow-200 dark:text-gray-800" aria-hidden="true" />
          </PopoverButton>

          <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-screen max-w-md overflow-hidden rounded-3xl bg-gray-200 shadow-lg ring-1 ring-gray-900/5">
              <div class="p-4">
                <div v-for="item in products" :key="item.name" class="group relative flex gap-x-6 rounded-lg p-4 text-sm leading-6 hover:bg-gray-50">
                  <div class="mt-1 flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                    <component :is="item.icon" class="h-8 w-8 text-gray-600 group-hover:text-yellow-600 stroke-1" aria-hidden="true" />
                  </div>
                  <div class="flex-auto">
                    <NuxtLink :to="localePath(item.href)" class="block font-semibold text-gray-900">
                      {{ item.name }}
                      <span class="absolute inset-0" />
                    </NuxtLink>
                    <p class="mt-1 text-gray-600">{{ item.description }}</p>
                  </div>
                </div>
              </div>
              <div class="grid grid-cols-2 divide-x divide-gray-900/5 bg-gray-50">
                <NuxtLink v-for="item in callsToAction" :key="item.name" :to="localePath(item.href)" class="flex items-center justify-center gap-x-2.5 p-3 text-sm font-semibold leading-6 text-gray-900 hover:bg-gray-100">
                  <component :is="item.icon" class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
                  {{ item.name }}
                </NuxtLink>
              </div>
            </PopoverPanel>
          </transition>
        </Popover>



        <Popover class="relative">
          <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-yellow-400 dark:text-black">
            Transfer
            <ChevronDownIcon class="h-5 w-5 flex-none text-yellow-200 dark:text-gray-800" aria-hidden="true" />
          </PopoverButton>

          <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-screen max-w-md overflow-hidden rounded-3xl bg-gray-200 shadow-lg ring-1 ring-gray-900/5">
              <div class="p-4">
                <div v-for="item in transfers" :key="item.name" class="group relative flex gap-x-6 rounded-lg p-4 text-sm leading-6 hover:bg-gray-50">
                  <div class="mt-1 flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                    <component :is="item.icon" class="h-8 w-8 text-gray-600 group-hover:text-yellow-600 stroke-1" aria-hidden="true" />
                  </div>
                  <div class="flex-auto">
                    <NuxtLink :to="localePath(item.href)" class="block font-semibold text-gray-900">
                      {{ item.name }}
                      <span class="absolute inset-0" />
                    </NuxtLink>
                    <p class="mt-1 text-gray-600">{{ item.description }}</p>
                  </div>
                </div>
              </div>
              <div class="grid grid-cols-2 divide-x divide-gray-900/5 bg-gray-50">
                <NuxtLink v-for="item in callsToAction" :key="item.name" :to="localePath(item.href)" class="flex items-center justify-center gap-x-2.5 p-3 text-sm font-semibold leading-6 text-gray-900 hover:bg-gray-100">
                  <component :is="item.icon" class="h-5 w-5 flex-none text-gray-400" aria-hidden="true" />
                  {{ item.name }}
                </NuxtLink>
              </div>
            </PopoverPanel>
          </transition>
        </Popover>



          <NuxtLink
            class="text-sm font-semibold leading-6 text-yellow-400 dark:text-black"
            :to="localePath('/shop')"
          >
            Shop
          </NuxtLink>

          <NuxtLink
            class="text-sm font-semibold leading-6 text-yellow-400 dark:text-black"
            :to="localePath('/contact')"
          >
            Contact
          </NuxtLink>




          <!-- <Popover class="relative">
          <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-yellow-400 dark:text-black">
            Development 
            <ChevronDownIcon class="h-5 w-5 flex-none text-yellow-200 dark:text-gray-800" aria-hidden="true" />
          </PopoverButton>

          <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-96 rounded-3xl bg-gray-200 p-4 shadow-lg ring-1 ring-gray-900/5">
              <div v-for="item in development" :key="item.name" class="relative rounded-lg p-4 hover:bg-gray-50">
                <a :href="item.href" class="block text-sm font-semibold leading-6 text-gray-900">
                  {{ item.name }}
                  <span class="absolute inset-0" />
                </a>
                <p class="mt-1 text-sm leading-6 text-gray-600">{{ item.description }}</p>
              </div>
            </PopoverPanel>
          </transition>
        </Popover> -->







          <!-- <Popover class="relative">
          <PopoverButton class="flex items-center gap-x-1 text-sm font-semibold leading-6 text-yellow-400 dark:text-black">
            Network
            <ChevronDownIcon class="h-5 w-5 flex-none text-yellow-200 dark:text-gray-800" aria-hidden="true" />
          </PopoverButton>

          <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
            <PopoverPanel class="absolute -left-8 top-full z-10 mt-3 w-96 rounded-3xl bg-gray-200 p-4 shadow-lg ring-1 ring-gray-900/5">
              <div v-for="item in company" :key="item.name" class="relative rounded-lg p-4 hover:bg-gray-50">
                <a :href="item.href" class="block text-sm font-semibold leading-6 text-gray-900">
                  {{ item.name }}
                  <span class="absolute inset-0" />
                </a>
                <p class="mt-1 text-sm leading-6 text-gray-600">{{ item.description }}</p>
              </div>
            </PopoverPanel>
          </transition>
        </Popover> -->


      </PopoverGroup>
      <div class="hidden lg:flex lg:flex-1 lg:justify-end">


        <Language />


          <a
            href="https://lightning-dev.pages.dev"
            class="text-sm font-semibold leading-6 text-yellow-400 dark:text-black"
          >
            Login<span aria-hidden="true">&rarr;</span>
      </a>

      </div>
    </nav>
    <Dialog
      as="div"
      class="lg:hidden"
      @close="mobileMenuOpen = false"
      :open="mobileMenuOpen"
    >
      <div class="fixed inset-0 z-10" />
      
      <DialogPanel
        class="fixed inset-y-0 right-0 z-10 w-full overflow-y-auto bg-colorBgLight dark:bg-colorBgDark p-3 lg:px-8 sm:max-w-sm sm:ring-1 sm:ring-gray-900/10"
      >
        <div class="flex items-center justify-between">
          <NuxtLink to="/" class="-m-1.5 p-1.5">
            <span class="sr-only">Codex.eu.com</span>

            <img
            class="h-12 w-auto hidden dark:block"
            src="/logo-bright.png"
            alt=""
          />

          <img
            class="h-12 w-auto dark:hidden block"
            src="/logo-light.png"
            alt=""
          />

        </NuxtLink>
          <button
            type="button"
            class="-m-2.5 rounded-md p-2.5 text-gray-700 text-white dark:text-black"
            @click="mobileMenuOpen = false"
          >
            <span class="sr-only">Close menu</span>
            <XMarkIcon class="h-6 w-6" aria-hidden="true" />
          </button>
        </div>
        <div class="mt-6 flow-root px-3">

            <div class="flex flex-row py-4 justify-between">
              <NuxtLink v-for="item in products" :key="item.name"  :to="item.href" class="block text-xs font-semibold text-yellow-400 dark:text-black text-center" @click="mobileMenuOpen = false">
                {{ item.name }}
                <span class="mx-auto mt-1 flex h-11 w-11 flex-none items-center justify-center rounded-lg bg-gray-50 group-hover:bg-white">
                <component :is="item.icon" class="h-8 w-8 text-gray-600 group-hover:text-yellow-600 stroke-1" aria-hidden="true" />
                </span>
              </NuxtLink>
            </div> 

          <div class="-my-6 divide-y divide-white dark:divide-black">
            <div class="space-y-2 py-6">

              <NuxtLink
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-yellow-400 dark:text-black"
                  :to="localePath('/')"
                  @click="mobileMenuOpen = false"
                >
            Home
          </NuxtLink>

          <NuxtLink
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-yellow-400 dark:text-black"
                  :to="localePath('/bitcoin')"
                  @click="mobileMenuOpen = false"
                >
            Bitcoin
          </NuxtLink>

          <NuxtLink
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-yellow-400 dark:text-black"
                  :to="localePath('/shop')"
                  @click="mobileMenuOpen = false"
                >
            Shop
          </NuxtLink>

          <NuxtLink
                  class="-mx-3 block rounded-lg px-3 py-2 text-base font-semibold leading-7 text-yellow-400 dark:text-black"
                  :to="localePath('/contact')"
                  @click="mobileMenuOpen = false"
                >
            Contact
          </NuxtLink>

            </div>

            <div class="py-6">
                <a
                  href="https://lightning-dev.pages.dev"
                  class="-mx-3 block rounded-lg px-3 py-2.5 text-base font-semibold leading-7 text-yellow-400 dark:text-black"
                >
                  Login<span aria-hidden="true">&rarr;</span>
            </a>

            </div>
          </div>
        </div>
      </DialogPanel>
    </Dialog>
  </header>
</template>
<script setup>
</script>