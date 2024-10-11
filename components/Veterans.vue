<template>
    <div class="bg-gray-100 py-24 sm:py-32">
      <div class="mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:text-center">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Senior & Veteran Services</h2>
          <p class="mt-6 text-lg leading-8 text-gray-600">
            Tranquity Haven offers safe housing solutions using a shared home environment in partnership with community resources. Explore our Services below to find out more.
          </p>
        </div>
        <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
          <dl class="grid grid-cols-1 gap-x-8 gap-y-10 lg:grid-cols-2">
            <div v-for="service in services" :key="service.title" class="relative bg-white p-8 rounded-2xl shadow-lg">
              <dt class="text-base font-semibold leading-7 text-gray-900">
                <div class="mb-6 flex h-10 w-10 items-center justify-center rounded-lg bg-indigo-600">
                  <component :is="service.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                </div>
                {{ service.title }}
              </dt>
              <dd class="mt-2 text-base leading-7 text-gray-600">{{ service.description }}</dd>
              <div class="mt-4">
                <a href="#" class="text-sm font-semibold leading-6 text-indigo-600 hover:text-indigo-500">
                  Learn More <span aria-hidden="true">→</span>
                </a>
              </div>
            </div>
          </dl>
        </div>
      </div>
    </div>
  </template>
  
  <script setup>
  import { UserGroupIcon, HomeIcon } from '@heroicons/vue/24/outline'
  
  const services = [
    {
      title: 'For Case Managers',
      description: 'We work with social workers, case managers and faith-based organizations who work directly with displaced individuals who are in immediate need of housing.',
      icon: UserGroupIcon,
    },
    {
      title: 'For Real Estate Agents',
      description: 'We work with homeowners and real estate professionals that have access to vacant or distressed properties to offer a tenancy solution while serving the community.',
      icon: HomeIcon,
    },
  ]
  </script>