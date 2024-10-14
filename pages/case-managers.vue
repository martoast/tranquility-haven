<template>
    <div>
      <div class="isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0">
        <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-10">
          <div class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
            <div class="lg:pr-4">
              <div class="lg:max-w-lg">
                <p class="text-base font-semibold leading-7 text-primary">Services for Case Managers</p>
                <h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Supporting Displaced Individuals</h1>
                <p class="mt-6 text-xl leading-8 text-gray-700">We work with social workers, case managers and faith-based organizations who work directly with displaced individuals who are in immediate need of housing.</p>
              </div>
            </div>
          </div>
          <div class="-ml-12 -mt-12 p-12 lg:sticky lg:top-4 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden">
            <img class="w-[48rem] max-w-none rounded-xl bg-gray-900 shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]" src="/case-managers-impact.jpg" alt="Case managers working with clients" />
          </div>
          <div class="lg:col-span-2 lg:col-start-1 lg:row-start-2 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
            <div class="lg:pr-4">
              <div class="max-w-xl text-base leading-7 text-gray-700 lg:max-w-lg">
                <p>Our homes specialize in serving seniors and veterans receiving Disability, SSI, and SSDI benefits. We provide gender-specific living arrangements tailored to their unique needs.</p>
                <h2 class="mt-16 text-2xl font-bold tracking-tight text-gray-900">Reasons to Choose Us</h2>
                <ul role="list" class="mt-8 space-y-8 text-gray-600">
                  <li class="flex gap-x-3">
                    <PlusIcon class="mt-1 h-5 w-5 flex-none text-primary" aria-hidden="true" />
                    <span>
                      <strong class="font-semibold text-gray-900">Safe, Stable Environment.</strong> We offer a clean and sober, structured environment with private rooms and shared bathrooms. All utilities paid, cable, wifi, furnished bedroom with linens, and groceries. Our properties are located in quiet, clean neighborhoods with access to public transportation.
                    </span>
                  </li>
                  <li class="flex gap-x-3">
                    <PlusIcon class="mt-1 h-5 w-5 flex-none text-primary" aria-hidden="true" />
                    <span>
                      <strong class="font-semibold text-gray-900">Worry-Free Living.</strong> All utilities are paid including cable and wifi. We also offer a furnished bedroom, clean linens and groceries. Transportation may also be available to medical appointments.
                    </span>
                  </li>
                </ul>
                <p class="mt-8">At Tranquility Haven, we're committed to providing a supportive and comfortable living environment for seniors and veterans in need. Our partnership with case managers and social workers allows us to address the immediate housing needs of displaced individuals effectively.</p>
                <p class="mt-6">By choosing our services, you're ensuring that your clients receive not just a place to stay, but a home where they can thrive and regain stability in their lives.</p>
              </div>
            </div>
          </div>
        </div>
      </div>
      <Contact/>
    </div>
  </template>
  
  <script setup>
  import { PlusIcon } from '@heroicons/vue/24/solid'
  </script>