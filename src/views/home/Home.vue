<template>
  <nav-bar class="nav-home">
    <div  slot="center">首页</div>
  </nav-bar>
</template>

<script>
import NavBar from 'components/common/navbar/NavBar'

export default {
  data () {
    return {
      
    }
  },
  components: {
    NavBar
  }
}
</script>

<style>
.nav-home {
  background-color: var(--color-tint);
  color: #fff;
}
</style>