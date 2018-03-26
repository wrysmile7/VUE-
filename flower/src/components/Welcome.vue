<template>
  <div class="countiner" :style="{top: beshow + 'px'}">
    <div class="warp">
      <header>
        <p @click.stop="handleMenu">
          <img src="../img/icon_dis_menu_wt@2x.png" v-if="bool">
          <img src="../img/icon_dis_close_wt@2x.png" v-if="!bool">
        </p>
      </header>
      <div class="cover-info">
        <div class="cover-logo"></div>
        <div class="cover-slogan"></div>
        <form class="cover-search">
          <div class="search-btn">
            <i></i>
          </div>
          <input type="text" v-model="searchText" placeholder="搜索你喜欢的">
        </form>
        <div class="cover-up" @click="handleUp"></div>
      </div>
    </div>
    <transition name="bond">
      <div class="cover-menu" v-if="!bool">
        <Menu></Menu>
      </div>
    </transition>
  </div>
</template>

<script>
import Menu from '@/components/Menu'

export default {
  name: 'Welcome',
  data () {
    return {
      bool:true,
      searchText: '',
      beshow:0
    }
  },
  methods:{
    handleMenu(){
      this.bool = !this.bool
    },
    handleUp(){
      this.beshow = -667
    }
  },
  components:{
    Menu
  }
}
</script>

<style>
  
</style>
