<script>
import { AdvancedImage, lazyload } from '@cloudinary/vue3';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'brown_sheep'.
const sheepImage = cld.image('brown_sheep');

// Instantiate a CloudinaryImage object for the image with the public ID, 'woman'.
const womanImage = cld.image('woman');

// Instantiate a CloudinaryImage object for the image with the public ID, 'fat_cat'.
const catImage = cld.image('fat_cat');

export default {
  components: {
    AdvancedImage,
  },
  data() {
    return {
        plugins: [lazyload()],
        sheepImage,
        womanImage,
        catImage,
    };
  },
};
</script>

<template>
  <div class="App-body">
    <h3>Using lazyload</h3>
    <p>Scroll down to see images lazy load</p>
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="sheepImage" :plugins="plugins"/>
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="womanImage" :plugins="plugins"/>
    <div class="bigspacer"></div>
    <AdvancedImage :cldImg="catImage" :plugins="plugins"/>
  </div>
</template>
