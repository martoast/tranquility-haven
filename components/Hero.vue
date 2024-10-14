<template>
  <div class="relative bg-gray-50">
    <main class="lg:relative">
      <div class="mx-auto w-full max-w-7xl pb-20 pt-16 text-center lg:py-48 lg:text-left">
        <div class="px-6 sm:px-8 lg:w-1/2 xl:pr-16">
          <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-5xl md:text-6xl lg:text-5xl xl:text-6xl">
            <span class="block xl:inline">Welcome to</span>
            {{ ' ' }}
            <span class="block text-primary xl:inline">Tranquility Haven</span>
          </h1>
          <p class="mx-auto mt-3 max-w-md text-lg text-gray-500 sm:text-xl md:mt-5 md:max-w-3xl">A nurturing community where seniors and veterans can thrive, connect, and find the care they deserve.</p>
          <div class="mt-10 sm:flex sm:justify-center lg:justify-start">
            <div class="rounded-md shadow">
              <a href="#contact" class="flex w-full items-center justify-center rounded-md border border-transparent bg-primary px-8 py-3 text-base font-medium text-white hover:bg-primary-light md:px-10 md:py-4 md:text-lg">Contact us</a>
            </div>
            <div class="mt-3 rounded-md shadow sm:ml-3 sm:mt-0">
              <a href="#benefits" class="flex w-full items-center justify-center rounded-md border border-transparent bg-white px-8 py-3 text-base font-medium text-primary hover:bg-gray-50 md:px-10 md:py-4 md:text-lg">Learn more</a>
            </div>
          </div>
        </div>
      </div>
      <div class="relative h-64 w-full sm:h-72 md:h-96 lg:absolute lg:inset-y-0 lg:right-0 lg:h-full lg:w-1/2">
        <img class="absolute inset-0 h-full w-full object-cover" src="/diversity.jpg" alt="Diverse group of seniors and veterans" />
      </div>
    </main>
  </div>
</template>

