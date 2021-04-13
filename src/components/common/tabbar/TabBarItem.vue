<template>
  <div class="tab-bar-item" @click="itemClick()">
    <div v-if="!isActived">
      <slot name="item-icon"></slot>
    </div>
    <div v-else>
      <slot name="item-icon-sel"></slot>
    </div>
    <div :style="activeStyle">
      <slot name="item-title"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TabBarItem',
  props: {
    path: String,
    activeColor: {
      type: String,
      default: 'rgba(212, 35, 122, 1)'
    }
  },
  data() {
    return {
    }
  },
  methods: {
    itemClick() {
      if(this.$route.path !== this.path){
        this.$router.replace(this.path)
      }
    }
  },
  computed: {
    isActived() {
      return this.$route.path.indexOf(this.path) !== -1
    },
    activeStyle() {
      return this.isActived ? {color: this.activeColor} : {}
    }
  }
}
</script>

<style>
  .tab-bar-item {
    flex: 1;
    text-align: center;
    height: 49px;
    background-color: rgb(243, 243, 243);

    font-size: 12px;
    font-family: '楷体';
  }

  .tab-bar-item img {
    margin-top: 5px;
    vertical-align: middle;
    width: 24px;
    height: 24px;
  }
</style>