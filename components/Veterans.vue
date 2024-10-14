<template>
  <div id="services" class="bg-gray-100 py-24 sm:py-32">
    <div class="mx-auto max-w-7xl px-6 lg:px-8">
      <div class="mx-auto max-w-2xl lg:text-center">
        <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Compassionate Care for Seniors & Veterans</h2>
        <p class="mt-6 text-lg leading-8 text-gray-600">
          Our innovative shared home approach, combined with strong community partnerships, ensures a supportive and enriching living experience.
        </p>
      </div>
      <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
        <dl class="grid grid-cols-1 gap-x-8 gap-y-10 lg:grid-cols-2">
          <div v-for="service in services" :key="service.title" class="relative bg-white rounded-2xl shadow-lg overflow-hidden">
            <div class="aspect-w-16 aspect-h-9">
              <img :src="service.image" :alt="service.title" class="object-cover w-full h-full" />
            </div>
            <div class="p-8">
              <dt class="text-base font-semibold leading-7 text-gray-900">
                {{ service.title }}
              </dt>
              <dd class="mt-2 text-base leading-7 text-gray-600">{{ service.description }}</dd>
              <div class="mt-4">
                <a :href="service.href" class="text-sm font-semibold leading-6 text-primary hover:text-primary-light">
                  Learn More <span aria-hidden="true">→</span>
                </a>
              </div>
            </div>
          </div>
        </dl>
      </div>
    </div>
  </div>
</template>

<script setup>
const services = [
  {
    title: 'Case Managers',
    description: 'We work with social workers, case managers and faith-based organizations who work directly with displaced individuals who are in immediate need of housing.',
    image: '/faith.jpeg', // Replace with your image path
    href: '/case-managers'
  },
  {
    title: 'Landlords & Realtors',
    description: 'We work with homeowners and real estate professionals that have access to vacant or distressed properties to offer a tenancy solution while serving the community.',
    image: '/agents.jpg', // Replace with your image path
    href: '/landlords'
  },
  {
    title: 'Seniors & Veterans',
    description: 'If you are a senior or a veteran in need of affordable housing, we can help you',
    image: '/veteran.jpg',
    href: '/veterans'
  }
]
</script>