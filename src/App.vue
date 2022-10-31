<script setup>
import DefaultAdvancedImage from './components/DefaultAdvancedImage.vue';
import DefaultAccessibility from './components/DefaultAccessibility.vue';
import LazyLoad from './components/LazyLoad.vue';
import Responsive from './components/Responsive.vue';
import Accessibility from './components/Accessibility.vue';
import LazyLoadPlaceholder from './components/LazyLoadPlaceholder.vue';
</script>

<template>
  <div class="App-body">
  <h1>Vue Plugins</h1>
  </div>
  <DefaultAdvancedImage />
  <div class="spacer"></div>
  <DefaultAccessibility />
  <div class="spacer"></div>
  <Accessibility />
  <div class="spacer"></div>
  <Responsive />
  <div class="spacer"></div>
  <LazyLoad />
  <div class="spacer"></div>
  <LazyLoadPlaceholder />
</template>

<style>
.App-body {
  text-align: center;
  font-size: calc(8px + 2vmin);
  color: black;
}

div.spacer {
  height: 20px;
}

div.bigspacer {
  height: 700px;
}

.App-link {
  color: #FF5050;
}

a:hover {
  color: #FF5050;
  text-decoration: underline;
}

img {
	max-width: 50%;
}

video {
	max-width: 50%;
}
</style>
