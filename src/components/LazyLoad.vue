<script setup>
import { AdvancedImage, lazyload } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate CloudinaryImage objects.
const sheepImage = cld.image('brown_sheep');
const womanImage = cld.image('woman');
const catImage = cld.image('fat_cat');

// Define plugins.
const plugins = [lazyload()];

</script>

<template>
  <div class="App-body">
    <h3>Using lazyload</h3>
    <p>Scroll down to see images lazy load</p>
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="sheepImage" :plugins="plugins" />
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="womanImage" :plugins="plugins" />
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="catImage" :plugins="plugins" />
  </div>
</template>
