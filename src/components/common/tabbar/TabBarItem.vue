<!--  -->
<template>
    <div class="tab-bar-item" @click="itemClick">
      <div v-if="!isActive"><slot name="item-icon"></slot></div>
      <div v-else><slot name="item-icon_active"></slot></div>
      <!-- <div :class="{activeClass: isActive}"><slot name="item-text"></slot></div> -->
      <!-- 进行进一步的封装，在使用该组件时可以通过activeColor更改颜色 -->
      <div :style="activeStyle"><slot name="item-text"></slot></div>
      <!-- <slot></slot> -->
    </div>
</template>

<script>
export default {
  data () {
    return {
      // isActive: true,    
    }
  },
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'red'
    }
  },
  computed: {
    isActive() {
      //$route 当前处于活跃的路由对象
      //判断当前活跃的路由的path中是否有item中的this.path
      //indexOf() == -1 表示查找的值没有出现
      return this.$route.path.indexOf(this.path) !== -1;
    },
    activeStyle() {
      return this.isActive ? {'color' : this.activeColor} : {};
    }
  },
  methods: {
    itemClick() {
      // this.$router.push()
      // console.log(this.path);
      this.$router.replace(this.path);
    }
  }
}
</script>

<style  scoped>
.tab-bar-item {
  flex: 1;
  text-align: center;
  height: 49px; /*tabbar 大部分设置为49px*/
  margin-top: 3px;
}
.tab-bar-item img {
  width: 24px;
  height: 24px;
  vertical-align: middle;
}
.activeClass {
  color: red;
}
</style>
