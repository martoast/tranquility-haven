<template>
    <div class="bg-white py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <h2 class="text-base font-semibold leading-7 text-primary">Our Services</h2>
          <p class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Housing Solutions in a Shared Environment</p>
          <p class="mt-6 text-lg leading-8 text-gray-600">Tranquility Haven offers housing solutions using a shared home environment in partnership with community resources. Explore our Services below to find out more.</p>
        </div>
        <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
          <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
            <div v-for="service in services" :key="service.name" class="relative pl-16">
              <dt class="text-base font-semibold leading-7 text-gray-900">
                <div class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-primary">
                  <component :is="service.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                </div>
                {{ service.name }}
              </dt>
              <dd class="mt-2 text-base leading-7 text-gray-600">{{ service.description }}</dd>
            </div>
          </dl>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { HomeIcon, UsersIcon, WifiIcon, HeartIcon } from '@heroicons/vue/24/outline'
  
  const services = [
    {
      name: 'Room & Board',
      description: 'Offering a safe and clean living space.',
      icon: HomeIcon,
    },
    {
      name: 'Community',
      description: 'Building togetherness, self-reliance, and a strong community to reach personal goals.',
      icon: UsersIcon,
    },
    {
      name: 'Free Wifi',
      description: 'Enjoy complimentary high-speed Wi-Fi access at our facility.',
      icon: WifiIcon,
    },
    {
      name: 'Supportive Services',
      description: 'Providing a nurturing space and guiding you to local help and resources.',
      icon: HeartIcon,
    },
  ]
  </script>