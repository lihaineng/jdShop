<template>
    <div>
      <div class="wrapper">
        <StaticPart/>
        <Nearby />
      </div>
      <Docker />
    </div>
  </template>

  
<script>
import Docker from './Docker.vue'
import Nearby from './Nearby.vue'
import StaticPart from './StaticPart.vue'
export default {
  name: 'Home',
  components: {StaticPart, Docker, Nearby}
}
</script>
  
<style lang="scss" scoped>
  @import '../../style/viriables.scss';
  @import '../../style/mixins.scss';
  .wrapper {
    position: absolute;
    left: 0;
    top: 0;
    bottom: .5rem;
    right: 0;
    padding: 0 .18rem;
  }
</style>
  