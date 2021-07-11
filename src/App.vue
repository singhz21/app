<template>
  <div id="app">
    <Header />
    <div class="container">
      <router-view/>
    </div>
  </div>
</template>

<script>
import Header from './components/Header.vue'

export default {
  components: {
    Header   
  }
}
</script>


<style>
body {
  background: #fff;
}

.container {
  max-width: 900px;
 }

.card {
  background: #eee;
}

.card-body {
  color: #000;
}

.card-body a {
  color: #41b883;
}
</style>
