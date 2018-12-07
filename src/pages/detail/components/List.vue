<template>
    <div>
      <div class="item" v-for="(item, index) of list" :key="index">
          <div class="item-title border-bottom">
              <span class="iconfont">&#xe748;</span>
              {{item.groupName}}
          </div>
          <div v-if="item.groupDis" class="item-groupDis">
            <detail-list :list="item.groupDis">
            </detail-list>
          </div>
      </div>
    </div>
</template>

<script>
export default {
  name: 'DetailList',
  props: {
    list: Array
  }
}
</script>

<style lang="stylus" scoped>
  .iconfont
    position: relative;
    left: .06rem
    right: .06rem
    display: inline-block;
    width: .36rem;
    height: .36rem;
    margin-right: .1rem

  .item-title {
    line-height: .8rem
    font-size: .32rem
    padding: 0 .2rem
  }
  .item-groupDis
    padding: 0 .2rem
</style>
