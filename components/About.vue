<template>
    <div>
      <!-- Content section -->
      <div id="about" class="mx-auto py-24 sm:py-32 max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl lg:mx-0 lg:max-w-none">
          <h2 class="text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">About Tranquility Haven</h2>
          <div class="mt-6 flex flex-col gap-x-8 gap-y-20 lg:flex-row">
            <div class="lg:w-full lg:max-w-2xl lg:flex-auto">
              <p class="text-xl leading-8 text-gray-600">We believe in diversity, inclusion & equity</p>
              <div class="mt-10 max-w-xl text-base leading-7 text-gray-700">
                <p>From the moment you arrive at Tranquility Haven, you'll be embraced by our caring community. Our Co-living homes are a sanctuary for everyone, offering a supportive and inclusive environment.</p>
                <p class="mt-10">Whether you're seeking stability, comfort, or a fresh start, Tranquility Haven is here to provide flexible living arrangements tailored to your needs, ensuring your stay is comfortable and safe.</p>
              </div>
            </div>
            <div class="lg:flex lg:flex-auto lg:justify-center">
              <dl class="w-64 space-y-8 xl:w-80">
                <div v-for="stat in stats" :key="stat.label" class="flex flex-col-reverse gap-y-4">
                  <dt class="text-base leading-7 text-gray-600">{{ stat.label }}</dt>
                  <dd class="text-5xl font-semibold tracking-tight text-gray-900">{{ stat.value }}</dd>
                </div>
              </dl>
            </div>
          </div>
        </div>
      </div>
  
      <!-- Image section -->
      <div class="mt-12 xl:mx-auto xl:max-w-7xl xl:px-8">
        <img src="https://static.wixstatic.com/media/11062b_6ba82d84d8ca4a9b9b3fb52426424e9c~mv2.jpg/v1/fill/w_2842,h_1600,al_c,q_90,usm_0.66_1.00_0.01/11062b_6ba82d84d8ca4a9b9b3fb52426424e9c~mv2.jpg" alt="Tranquility Haven Community" class="aspect-[5/2] w-full object-cover xl:rounded-3xl" />
      </div>
    </div>
  </template>
  
  <script setup>
  const stats = [
    { label: 'Co-living Homes', value: '15+' },
    { label: 'Residents Housed', value: '100+' },
    { label: 'Community Partners', value: '20+' },
  ]
  </script>