<script setup>
import { AdvancedImage } from '@cloudinary/vue';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'sample'.
const myImage = cld.image('sample');

</script>

<template>
  <div class="App-body">
    <h3>Render an image in the AdvancedImage component</h3>
    <AdvancedImage :cldImg="myImage" />
  </div>
</template>
