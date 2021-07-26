<template>
  <div id="tab-bar">
    <slot></slot>
  </div>
</template>

<script>
export default {

}
</script>

<style>
#tab-bar {
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: #f6f6f6;
  /*盒子阴影   x轴方向 y轴方向 模糊长度 */
  box-shadow: 0 -2px 2px rgba(0, 0, 0, .2);
  
}

</style>