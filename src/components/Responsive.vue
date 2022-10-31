<script>
import { AdvancedImage, responsive } from '@cloudinary/vue3';
import { Cloudinary } from '@cloudinary/url-gen';

// Create a Cloudinary instance and set your cloud name.
const cld = new Cloudinary({
  cloud: {
    cloudName: 'demo',
  },
});

// Instantiate a CloudinaryImage object for the image with the public ID, 'sample'.
const myImage = cld.image('sample');

export default {
  components: {
    AdvancedImage,
  },
  data() {
    return {
        plugins: [responsive({steps: 100})],
        myImage,
    };
  },
};
</script>

<template>
  <div class="App-body">
    <h3>Using responsive</h3>
    <p>Resize window to see changes (100 is the step size in px)</p>
    <AdvancedImage :cldImg="myImage" :plugins="plugins"/>
  </div>
</template>
