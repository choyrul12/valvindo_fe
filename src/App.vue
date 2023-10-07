<script>
import  Navbar  from './components/Navbar.vue';
import  Footers from './components/Footer.vue';
export default {
  components: {
    Navbar,
    Footers,
  },
};
</script>

<template>
  <Navbar/>
    <RouterView />
  <Footers />
</template>

