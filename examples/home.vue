<template>
  <section>
    <s-list v-for="group in navs">
      <span slot="title">{{group.title}}</span>
      <s-list-item v-for="item in group.list" :to="item.path" navigate>
        {{ item.name }}
      </s-list-item>
    </s-list>
  </section>
</template>

<script type="text/babel">
import navs from './navs.json'

export default {
  data() {
    return {
      navs: []
    }
  },

  created() {
    this.navs = navs
  }
}
</script>

<style lang="less" scoped>
  @import "../src/less/src/variables.less";
  li{list-style: none;}
</style>
