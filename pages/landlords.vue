<template>
    <div>
      <div class="isolate overflow-hidden bg-white px-6 py-24 sm:py-32 lg:overflow-visible lg:px-0">
        <div class="mx-auto grid max-w-2xl grid-cols-1 gap-x-8 gap-y-16 lg:mx-0 lg:max-w-none lg:grid-cols-2 lg:items-start lg:gap-y-10">
          <div class="lg:col-span-2 lg:col-start-1 lg:row-start-1 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
            <div class="lg:pr-4">
              <div class="lg:max-w-lg">
                <p class="text-base font-semibold leading-7 text-primary">Services for Landlords & Realtors</p>
                <h1 class="mt-2 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">Partnering for Community Solutions</h1>
                <p class="mt-6 text-xl leading-8 text-gray-700">Landlords with available properties, along with Realtors holding pocket listings of vacant or distressed homes, can collaborate with us to provide community-serving solutions.</p>
              </div>
            </div>
          </div>
          <div class="-ml-12 -mt-12 p-12 lg:sticky lg:top-4 lg:col-start-2 lg:row-span-2 lg:row-start-1 lg:overflow-hidden">
            <img class="w-[48rem] max-w-none rounded-xl bg-gray-900 shadow-xl ring-1 ring-gray-400/10 sm:w-[57rem]" src="/agents.jpg" alt="Landlords and Realtors partnering for community housing" />
          </div>
          <div class="lg:col-span-2 lg:col-start-1 lg:row-start-2 lg:mx-auto lg:grid lg:w-full lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
            <div class="lg:pr-4">
              <div class="max-w-xl text-base leading-7 text-gray-700 lg:max-w-lg">
                <p>Partner with us to utilize your space for housing our clients, contributing to a meaningful cause while fulfilling your property's potential.</p>
                <h2 class="mt-16 text-2xl font-bold tracking-tight text-gray-900">Reasons to Choose Us</h2>
                <ul role="list" class="mt-8 space-y-8 text-gray-600">
                  <li class="flex gap-x-3">
                    <PlusIcon class="mt-1 h-5 w-5 flex-none text-primary" aria-hidden="true" />
                    <span>
                      <strong class="font-semibold text-gray-900">Guaranteed rent payments.</strong> Lease or sublet the property to us for at least 24 months, receive a higher rental rate from the HUD-VASH program which is similar to Section-8 but for seniors & veterans.
                    </span>
                  </li>
                  <li class="flex gap-x-3">
                    <PlusIcon class="mt-1 h-5 w-5 flex-none text-primary" aria-hidden="true" />
                    <span>
                      <strong class="font-semibold text-gray-900">Worry-Free Property Maintenance.</strong> We are responsible for all maintenance, repairs and property upkeep. No need for evictions, our Seniors & Veterans are usually under case-management and they have their policies and procedures for removal of non-compliant clients.
                    </span>
                  </li>
                </ul>
                <p class="mt-8">By partnering with Tranquility Haven, you're not just renting out your property – you're contributing to a vital community service. Your property becomes a home for seniors and veterans in need, while you enjoy the benefits of guaranteed payments and hassle-free property management.</p>
                <p class="mt-6">Join us in making a difference. Your property could be the key to providing stable, comfortable housing for those who need it most, all while ensuring a reliable return on your investment.</p>
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