<template>
  <NavparMain />
  <router-view/>
</template>
<script>
import NavparMain from './components/NavparMain.vue';
export default {
  name: 'app',
  components:{NavparMain}
}
</script>

