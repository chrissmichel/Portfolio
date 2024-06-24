<template navbar>
<ul class="nav">
  <li class="nav-item">
    <a class="nav-link active" v-bind:href="/projects/" aria-current="page">Projects</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" v-bind:href="/about/" @click="isClicked(about)">About Me</a>
  </li>
  <li class="nav-item">
    <a class="nav-link" v-bind:href="/blog/">Blog</a>
  </li>
</ul>
</template>

<script>
export default {
  name: 'navbar',
  data() {
    return {
      projects: true,
      about: true,
      blog: true
    };
  },
  methods: {
    isClicked(elem){
      elem = !elem;
      return  console.log(elem);
    }
  }
};
</script>