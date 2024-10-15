<template>
  <div id="contact" class="relative bg-white">
    <div class="absolute inset-0">
      <div class="absolute inset-y-0 left-0 w-1/2 bg-gray-50" />
    </div>
    <div class="relative mx-auto max-w-7xl lg:grid lg:grid-cols-5">
      <div class="bg-gray-50 px-6 py-16 lg:col-span-2 lg:px-8 lg:py-24 xl:pr-12">
        <div class="mx-auto max-w-lg">
          <h2 class="text-2xl font-bold tracking-tight text-gray-900 sm:text-3xl">
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
                <PhoneIcon class="h-6 w-6 flex-shrink-0 text-gray-400" aria-hidden="true" />
                <a href="tel:+14049541468" class="ml-3 text-blue-600 hover:text-blue-800">
                  404-954-1468
                </a>
              </dd>
            </div>
            <div class="mt-3">
              <dt class="sr-only">Email</dt>
              <dd class="flex">
                <EnvelopeIcon class="h-6 w-6 flex-shrink-0 text-gray-400" aria-hidden="true" />
                <a href="mailto:APlace2Reside@gmail.com" class="ml-3 text-blue-600 hover:text-blue-800">
                  APlace2Reside@gmail.com
                </a>
              </dd>
            </div>
          </dl>
        </div>
      </div>
      <div class="bg-white px-6 py-16 lg:col-span-3 lg:px-8 lg:py-24 xl:pl-12">
        <div class="mx-auto max-w-lg lg:max-w-none">
          <form @submit.prevent="submitForm" class="grid grid-cols-1 gap-y-6">
            <div class="grid grid-cols-1 gap-y-6 sm:grid-cols-2 sm:gap-x-8">
              <div>
                <label for="first-name" class="block text-sm font-medium text-gray-700">First name</label>
                <input
                  type="text"
                  v-model="form.firstName"
                  name="first-name"
                  id="first-name"
                  autocomplete="given-name"
                  class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500 sm:text-sm"
                />
              </div>
              <div>
                <label for="last-name" class="block text-sm font-medium text-gray-700">Last name</label>
                <input
                  type="text"
                  v-model="form.lastName"
                  name="last-name"
                  id="last-name"
                  autocomplete="family-name"
                  class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500 sm:text-sm"
                />
              </div>
            </div>
            <div>
              <label for="email" class="block text-sm font-medium text-gray-700">Email</label>
              <input
                id="email"
                v-model="form.email"
                name="email"
                type="email"
                autocomplete="email"
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500 sm:text-sm"
              />
            </div>
            <div>
              <label for="phone" class="block text-sm font-medium text-gray-700">Phone</label>
              <input
                type="tel"
                v-model="form.phone"
                name="phone"
                id="phone"
                autocomplete="tel"
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500 sm:text-sm"
              />
            </div>
            <div>
              <label for="message" class="block text-sm font-medium text-gray-700">Message</label>
              <textarea
                id="message"
                v-model="form.message"
                name="message"
                rows="4"
                class="mt-1 block w-full rounded-md border-gray-300 shadow-sm focus:border-primarylight-500 focus:ring-primarylight-500 sm:text-sm"
              ></textarea>
            </div>
            <div>
              <div class="flex items-start">
                <div class="flex-shrink-0">
                  <input v-model="form.privacyPolicy" id="privacy-policy" name="privacy-policy" type="checkbox" class="h-4 w-4 rounded border-gray-300 text-primary focus:ring-primary" />
                </div>
                <div class="ml-3">
                  <label for="privacy-policy" class="text-sm text-gray-500">
                    I agree to the <a href="#" class="font-medium text-gray-700 underline">privacy policy</a>
                  </label>
                </div>
              </div>
            </div>
            <div>
              <button
                type="submit"
                class="inline-flex w-full justify-center rounded-md border border-transparent bg-primary px-6 py-3 text-base font-medium text-white shadow-sm hover:bg-primarylight focus:outline-none focus:ring-2 focus:ring-primarylight-500 focus:ring-offset-2 sm:w-auto"
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
import { ref } from 'vue';
import { EnvelopeIcon, PhoneIcon } from "@heroicons/vue/24/outline";

const form = ref({
  firstName: '',
  lastName: '',
  email: '',
  phone: '',
  message: '',
  privacyPolicy: false
});

const submitForm = async () => {
  if (validateForm()) {
    try {
      const payload = {
        lead: {
          firstName: form.value.firstName,
          lastName: form.value.lastName,
          email: form.value.email,
          phone: form.value.phone,
          message: form.value.message
        }
      };

      console.log('Payload:', payload);

      const headers = {
        'Content-Type': 'application/json'
      };

      const response = await fetch('/.netlify/functions/leadWebhook', {
        method: 'POST',
        headers: headers,
        body: JSON.stringify(payload)
      });

      if (!response.ok) {
        throw new Error('Network response was not ok')
      }

      alert('Submitted!!! We will be in touch.')
      // Reset form
      form.value = {
        firstName: '',
        lastName: '',
        email: '',
        phone: '',
        message: '',
        privacyPolicy: false
      }
    } catch (error) {
      console.error('Error submitting form:', error)
      alert('An error occurred while submitting your data. Please try again.')
    }
  } else {
    alert('Please fill in all required fields and accept the privacy policy before submitting.')
  }
}

const validateForm = () => {
  return (
    form.value.firstName.trim() !== '' &&
    form.value.lastName.trim() !== '' &&
    form.value.email.trim() !== '' &&
    form.value.phone.trim() !== '' &&
    form.value.message.trim() !== '' &&
    form.value.privacyPolicy
  );
}
</script>