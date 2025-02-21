<script setup>
import { AdvancedImage, accessibility } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'sample'.
const myImage = cld.image('sample');

// Define plugins for accessibility with default settings.
const plugins = [accessibility()];

</script>

<template>
  <div class="App-body">
    <h3>Using default accessibility</h3>
    <AdvancedImage :cldImg="myImage" :plugins="plugins" />
  </div>
</template>
