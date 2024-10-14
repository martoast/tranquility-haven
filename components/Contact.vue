<template>
  <div id="contact" class="relative bg-white">
    <div class="absolute inset-0">
      <div class="absolute inset-y-0 left-0 w-1/2 bg-gray-50" />
    </div>
    <div class="relative mx-auto max-w-7xl lg:grid lg:grid-cols-5">
      <div
        class="bg-gray-50 px-6 py-16 lg:col-span-2 lg:px-8 lg:py-24 xl:pr-12"
      >
        <div class="mx-auto max-w-lg">
          <h2
            class="text-2xl font-bold tracking-tight text-gray-900 sm:text-3xl"
          >
            Get in touch
          </h2>
          <p class="mt-3 text-lg leading-6 text-gray-500">
            Whether you're seeking housing, want to partner with us, or just
            have questions, we're here to help.
          </p>
          <dl class="mt-8 text-base text-gray-500">
            <div>
              <dt class="sr-only">Postal address</dt>
              <dd>
                <p>1445 Woodmont Ln, NW, Ste. 4358,</p>
                <p>Atlanta GA 30318</p>
              </dd>
            </div>
            <div class="mt-6">
              <dt class="sr-only">Phone number</dt>
              <dd class="flex">
                <PhoneIcon
                  class="h-6 w-6 flex-shrink-0 text-gray-400"
                  aria-hidden="true"
                />
                <a
                  href="tel:+14049541468"
                  class="ml-3 text-blue-600 hover:text-blue-800"
                >
                  404-954-1468
                </a>
              </dd>
            </div>
            <div class="mt-3">
              <dt class="sr-only">Email</dt>
              <dd class="flex">
                <EnvelopeIcon
                  class="h-6 w-6 flex-shrink-0 text-gray-400"
                  aria-hidden="true"
                />
                <a
                  href="mailto:APlace2Reside@gmail.com"
                  class="ml-3 text-blue-600 hover:text-blue-800"
                >
                  APlace2Reside@gmail.com
                </a>
              </dd>
            </div>
          </dl>
        </div>
      </div>
      <div class="bg-white px-6 py-16 lg:col-span-3 lg:px-8 lg:py-24 xl:pl-12">
        <div class="mx-auto max-w-lg lg:max-w-none">
          <form action="#" method="POST" class="grid grid-cols-1 gap-y-6">
            <div>
              <label for="full-name" class="sr-only">Full name</label>
              <input
                type="text"
                name="full-name"
                id="full-name"
                autocomplete="name"
                class="block w-full rounded-md border-gray-300 px-4 py-3 placeholder-gray-500 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500"
                placeholder="Full name"
              />
            </div>
            <div>
              <label for="email" class="sr-only">Email</label>
              <input
                id="email"
                name="email"
                type="email"
                autocomplete="email"
                class="block w-full rounded-md border-gray-300 px-4 py-3 placeholder-gray-500 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500"
                placeholder="Email"
              />
            </div>
            <div>
              <label for="phone" class="sr-only">Phone</label>
              <input
                type="text"
                name="phone"
                id="phone"
                autocomplete="tel"
                class="block w-full rounded-md border-gray-300 px-4 py-3 placeholder-gray-500 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500"
                placeholder="Phone"
              />
            </div>
            <div>
              <label for="message" class="sr-only">Message</label>
              <textarea
                id="message"
                name="message"
                rows="4"
                class="block w-full rounded-md border-gray-300 px-4 py-3 placeholder-gray-500 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500"
                placeholder="Message"
              />
            </div>
            <div>
              <button
                type="submit"
                class="inline-flex justify-center rounded-md border border-transparent bg-primary px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-primarylight focus:outline-none focus:ring-2 focus:ring-primarylight-500 focus:ring-offset-2"
              >
                Submit
              </button>
            </div>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { EnvelopeIcon, PhoneIcon } from "@heroicons/vue/24/outline";
</script>
