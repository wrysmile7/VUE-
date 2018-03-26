<template>
	<div class="header_unit">
		<div class="mobile_header">
			<div class="logo icon-only">
				<a href="/" class="img" v-if="searchS==true"></a>
				<div class="mobile-title" v-if="searchS==true">发现</div>
			</div>
			<form class="search-form">
				<div class="header-button search">
					<i @click="handleSearch"></i>
				</div>
				<input type="text" class="search-input" v-if="searchS==false" v-model="searchInfo">
				<a class="cancel" v-if="searchS==false" @click="searchClose">
					<i></i>
				</a>
			</form>
			<a class="header-button menu" @click.stop="handleMenu" v-if="bool">
				<i></i>
			</a>
			<a class="header-button menu cross" @click.stop="handleMenu" v-if="!bool">
				<i></i>
			</a>
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
		data () {
			return {
				searchInfo:"",
				searchS:true,
				bool:true
			}
		},
		methods:{
			handleSearch(){
				this.searchS = !this.searchS;
				this.searchInfo = ""
			},
			searchClose(){
				this.searchS = true
			},
			handleMenu(){
				this.bool = !this.bool
			}
		},
		components:{
			Menu
		}
	}
</script>

<style>
	.header_unit {
	    position: fixed;
	    left: 0;
	    top: 0;
	    width: 100%;
	    z-index: 100;
	}
	.mobile_header {
	    position: relative;
	    background: #fff;
	    box-shadow: 0 0 4px rgba(0,0,0,.2);
	    width: 100%;
	    left: 0;
	    top: 0;
	    z-index: 99999;
	}
	.mobile_header .logo {
	    position: relative;
	    width: 100px;
	    height: 46px;
	}
	.mobile_header .logo.icon-only .img {
	    width: 25px;
	    display: inline-block;
	    margin-left: 10px;
	}
	.mobile_header .logo .img {
	    height: 44px;
	    background: url(../img/huaban_logo.png) 0 center no-repeat;
	    background-size: 75px;
	}
	.mobile_header .logo .mobile-title {
	    font-size: 18px;
	    display: inline-block;
	    position: absolute;
	    margin-left: 7px;
	    bottom: 12px;
	    white-space: nowrap;
	    width: 170px;
	    overflow: hidden;
	    text-overflow: ellipsis;
	}
	.mobile_header .header-button {
	    display: block;
	    position: absolute;
	    right: 44px;
	    top: 0;
	    width: 44px;
	    height: 44px;
	    z-index: 9
	}

	.mobile_header .header-button i {
	    position: absolute;
	    left: 50%;
	    top: 50%;
	    margin: -11px 0 0 -11px;
	    width: 22px;
	    height: 22px;
	    background: url(../img/topbar_icons.png) -59px 1px no-repeat
	}

	.mobile_header .header-button.menu {
	    right: 0;
	}
	.mobile_header .header-button.menu i {
	    background-position: -29px 1px;
	}
	.mobile_header .header-button.menu.cross{
		background: #f2f2f2;
	}
	.mobile_header .header-button.menu.cross i {
	    background-position: 0 1px;
	}

	.mobile_header .search-input {
	    height: 28px;
	    background-color: #F3F3F3;
	    border-radius: 0;
	    position: absolute;
	    top: 8px;
	    right: 44px;
	    padding: 0 8px;
	    border: 1px solid #DDD;
	    box-shadow: none;
	    outline: none;
	    font-size: 16px;
	    transition: opacity .2s linear;
	    box-sizing: border-box;
	}

	.mobile_header .search-input {
	    width: 74%;
	    opacity: 1;
	}

	.mobile_header .cancel {
	    display: block;
	    position: absolute;
	    left: 27%;
	    top: 0;
	    width: 40px;
	    height: 44px;
	    margin-left: -86px
	}

	.mobile_header .cancel i {
	    width: 20px;
	    height: 20px;
	    position: absolute;
	    background: url(../img/topbar_icons.png) 0 0 no-repeat;
	    position: absolute;
	    left: 50%;
	    top: 50%;
	    margin: -10px 0 0 -10px
	}

	.inner{
		background: #444 !important;
	}
</style>