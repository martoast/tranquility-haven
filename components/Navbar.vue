<template>
    <div>
      <nav class="relative bg-white shadow">
        <div class="mx-auto max-w-7xl px-6">
          <div class="flex items-center justify-between py-6">
            <div class="flex justify-start lg:w-0 lg:flex-1">
              <NuxtLink to="/">
                <span class="sr-only">Tranquility Haven</span>
                <img class="h-14 w-auto" src="/logo.svg" alt="Tranquility Haven Logo" />
              </NuxtLink>
            </div>
            <div class="hidden space-x-10 md:flex">
              <NuxtLink to="/" class="text-base font-medium text-gray-500 hover:text-gray-900">Home</NuxtLink>
              <NuxtLink to="/#about" class="text-base font-medium text-gray-500 hover:text-gray-900">About</NuxtLink>
              <PopoverGroup as="nav" class="hidden space-x-10 md:flex">
                <Popover class="relative" v-slot="{ open }">
                  <PopoverButton :class="[open ? 'text-gray-900' : 'text-gray-500', 'group inline-flex items-center rounded-md bg-white text-base font-medium hover:text-gray-900 focus:outline-none focus:ring-2 focus:ring-primary focus:ring-offset-2']">
                    <span>Solutions</span>
                    <ChevronDownIcon :class="[open ? 'text-gray-600' : 'text-gray-400', 'ml-2 h-5 w-5 group-hover:text-gray-500']" aria-hidden="true" />
                  </PopoverButton>
  
                  <transition enter-active-class="transition ease-out duration-200" enter-from-class="opacity-0 translate-y-1" enter-to-class="opacity-100 translate-y-0" leave-active-class="transition ease-in duration-150" leave-from-class="opacity-100 translate-y-0" leave-to-class="opacity-0 translate-y-1">
                    <PopoverPanel class="absolute z-10 -ml-4 mt-3 w-screen max-w-md transform px-2 sm:px-0 lg:left-1/2 lg:ml-0 lg:-translate-x-1/2">
                      <div class="overflow-hidden rounded-lg shadow-lg ring-1 ring-black ring-opacity-5">
                        <div class="relative grid gap-6 bg-white px-5 py-6 sm:gap-8 sm:p-8">
                          <NuxtLink v-for="item in features" :key="item.name" :to="item.href" class="-m-3 flex items-start rounded-lg p-3 hover:bg-gray-50">
                            <component :is="item.icon" class="h-6 w-6 flex-shrink-0 text-primary" aria-hidden="true" />
                            <div class="ml-4">
                              <p class="text-base font-medium text-gray-900">{{ item.name }}</p>
                              <p class="mt-1 text-sm text-gray-500">{{ item.description }}</p>
                            </div>
                          </NuxtLink>
                        </div>
                      </div>
                    </PopoverPanel>
                  </transition>
                </Popover>
              </PopoverGroup>
              <NuxtLink to="/#benefits" class="text-base font-medium text-gray-500 hover:text-gray-900">Benefits</NuxtLink>
              <NuxtLink to="/#contact" class="text-base font-medium text-gray-500 hover:text-gray-900">Contact</NuxtLink>
            </div>
            <div class="md:hidden">
              <button @click="toggleMobileMenu" class="inline-flex items-center justify-center p-2 rounded-md text-gray-400 hover:text-gray-500 hover:bg-gray-100 focus:outline-none focus:ring-2 focus:ring-inset focus:ring-primary">
                <span class="sr-only">Open main menu</span>
                <svg class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
                </svg>
              </button>
            </div>
          </div>
        </div>
        
        <!-- Mobile menu, show/hide based on menu state -->
        <div v-if="mobileMenuOpen" class="md:hidden">
          <div class="px-2 pt-2 pb-3 space-y-1 sm:px-3">
            <NuxtLink to="/" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Home</NuxtLink>
            <NuxtLink to="/#about" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">About</NuxtLink>
            <NuxtLink to="/#services" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Services</NuxtLink>
            <NuxtLink to="/#benefits" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Benefits</NuxtLink>
            <NuxtLink to="/#contact" class="block px-3 py-2 rounded-md text-base font-medium text-gray-700 hover:text-gray-900 hover:bg-gray-50">Contact</NuxtLink>
          </div>
        </div>
      </nav>
    </div>
  </template>

<script setup>
import { ref } from 'vue'
import { Popover, PopoverButton, PopoverGroup, PopoverPanel } from '@headlessui/vue'
import {
  UserGroupIcon,
  HomeIcon,
  UserIcon,
  Bars3Icon,
  XMarkIcon,
} from '@heroicons/vue/24/outline'
import { ChevronDownIcon } from '@heroicons/vue/20/solid'

const mobileMenuOpen = ref(false)

const toggleMobileMenu = () => {
  mobileMenuOpen.value = !mobileMenuOpen.value
};

const features = [
  {
    name: 'Case Managers',
    href: '/case-managers',
    description: 'Support for social workers and organizations helping those in need.',
    icon: UserGroupIcon,
  },
  {
    name: 'Landlords',
    href: '/landlords',
    description: 'Partner with us to provide community-serving housing solutions.',
    icon: HomeIcon,
  },
  {
    name: 'Veterans',
    href: '/veterans',
    description: 'Affordable housing options tailored for veterans.',
    icon: UserIcon,
  },
]
</script>