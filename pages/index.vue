<template>
    <div>
      <Hero/>
      
      <About/>
  
      <Services/>
      
      <Banner/>
  
      <Benefits/>
      
      <Veterans/>
      
      <Contact/>
    </div>
  </template>

<script setup>

useSeoMeta({
        robots: 'index, follow',
        title: 'Tranquility Haven',
        ogTitle: 'Tranquility Haven',
        author: 'Alex Martos',
        charset: 'utf-8',
        description: "A nurturing community where seniors and veterans can thrive, connect, and find the care they deserve.",
        ogDescription: "A nurturing community where seniors and veterans can thrive, connect, and find the care they deserve.",
        appleMobileWebAppCapable: 'yes',
        mobileWebAppCapable: 'yes',
        ogImage: '/diversity.jpg',
        ogLocaleAlternate: ['es_LA'],
        ogType: 'website',
        viewport: 'width=device-width, initial-scale=1',
    })

</script>
  