<script setup>
import { AdvancedImage, lazyload, placeholder } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'oil'.
const myImage = cld.image('oil');

// Define plugins for lazyloading and placeholder.
const plugins = [lazyload(), placeholder()];

</script>

<template>
  <div class="App-body">
    <h3>Using lazyload and placeholder</h3>
    <p>Scroll down to see image lazy load with placeholder</p>
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="myImage" :plugins="plugins" />
  </div>
</template>
