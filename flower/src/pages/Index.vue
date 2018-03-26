<template>
	<div>
		<Welcome v-if="bool"></Welcome>
		<div>
			<!-- <Header></Header> -->
		</div>
    <div>
      <Data></Data>
    </div>
	</div>
</template>

<script>
	import Welcome from '@/components/Welcome'
	import Header from '@/components/Header'
  import Data from '@/components/Data'
	export default {
	  name: 'Index',
	  data () {
	    return {
	    	bool:true
	    }
	  },
	  components:{
	  	Welcome,
	  	Header,
      Data
	  },
	  methods:{
	  	
	  }
	}
</script>

<style>
	.countiner{
    height: 100%;
    width: 100%;
    z-index: 999;
    position: absolute;
    transition: all .5s;
  }
  .warp{
    width: 100%;
    height: 100%;
    background: url(../img/welcome-bg.png) no-repeat;
    background-size: 100% 100%;
  }
  header{
    height: 16vw;
  }
  header p{
    display: block;
    position: absolute;
    right: 0;
    width: 8.5vw;
    height: 8.5vw;
    z-index: 9;
  }
  header p img{
    width: 5.87vw;
    height: 5.87vw;
    margin-top: 2.63vw;
  }
  .cover-info {
    position: relative;
    height: 75%;
    top: 28vw;
  }
  .cover-logo {
    background: url(../img/logo@2x.png) no-repeat center;
    background-size: cover;
    position: relative;
    margin: 0 auto 34px auto;
    width: 130px;
    height: 40px;
  }
  .cover-slogan {
    background: url(../img/info_dis_slogan@2x.png) no-repeat center;
    background-size: cover;
    position: relative;
    margin: 0 auto 25px auto;
    width: 264px;
    height: 24px;
  }
  .cover-search{
    position: relative;
    margin: 0 auto;
    width: 80%;
    height: 10.67vw;
  }
  .cover-search input{
    box-sizing: border-box;
    padding: 0 2.67vw;
    width: 100%;
    height: 100%;
    border: 0.27vw solid #fff;
    border-radius: 0.8vw;
    font-size: 4.8vw;
    color: #bbb;
    background: rgba(255,255,255,.9);
    outline: 0;
  }
  .search-btn{
    display: block;
    position: absolute;
    right: 0;
    width: 10.67vw;
    height: 10.67vw;
  }
  .search-btn i{
    display: inline-block;
    width: 7.47vw;
    height: 7.47vw;
    margin: 1.6vw 0 0 1.6vw;
    background: url(../img/icon_dis_search@2x.png) no-repeat;
    background-size: cover;
  }
  .search-btn:active i{
    background-position: 0 -70px
  }
  .cover-up{
    background: url(../img/info_dis_slideup@2x.png) no-repeat center;
    background-size: cover;
    position: relative;
    bottom: -250px;
    margin: 0 auto;
    width: 110px;
    height: 50px;
  }

  .cover-menu{
    width: 100%;
    height: 100%;
    position: absolute;
    top: 0;
    background: rgba(51,51,51,.95);
  }
  .bond-enter-active,.bond-leave-active{
    transition: all .5s;
  }
  .bond-enter,.bond-leave-to{
    opacity: 0;
  }
</style>