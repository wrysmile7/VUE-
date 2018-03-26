<template>
	<div class="inner">
		<div class="line login">
			<a class="signup-button btn rbtn">
				<span class="text"> 注册</span>
			</a>
			<a class="login-button btn">
				<span class="text"> 登录</span>
			</a>
		</div>
		<div class="line">
			<a class="link">最新</a>
			<i class="arrow"></i>
		</div>
		<div class="line">
			<a class="link">热门</a>
			<i class="arrow"></i>
		</div>
		<div class="line">
			<a class="link">发现</a>
			<i class="arrow"></i>
		</div>
	</div>
</template>

<script>
	export default {
	  name: 'Menu',
	  data () {
	    return {

	    }
	  }
	}
</script>

<style>
	.inner{
		background: 0;
	    margin-top: 44px;
	    box-shadow: 0 -44px 0 rgba(51,51,51,1);
	}
	.line{
		border-bottom: 1px solid #3B3B3B;
	    position: relative;
	    height: 44px;
	    line-height: 44px;
	    font-size: 16px;
	}
	.line.login {
	    padding: 20px;
	    height: 40px;
	    line-height: 40px;
	}
	.btn {
	    display: inline-block;
	    border-radius: 2px;
	    font-size: 16px;
	    background: linear-gradient( #FAFAFA, #F2F2F2);
	    border: 1px solid #D9D9D9;
	    cursor: pointer;
	    color: #444;
	    text-align: center;
	    font-weight: 700;
	}
	.line.login .btn {
	    width: 90px;
	    line-height: 36px;
	    height: 36px;
	    box-sizing: border-box;
	}
	.line.login .btn.signup-button {
	    width: 60%;
	    margin-right: 3.6%;
	    color: #fff;
	}
	.line.login .btn.login-button {
	    width: 35%;
	}
	.rbtn{
		background: linear-gradient( #E53E49, #D43636);
		border: 1px solid #C90000;

	}
	.line a.link {
	    display: block;
	    padding-left: 20px;
	    color: #DDD;
	}
	.line i.arrow{
		width: 16px;
	    height: 16px;
	    position: absolute;
	    right: 10px;
	    top: 50%;
	    margin-top: -8px;
	    background: url(../img/small_dark_right_arrow.png) 0 0 no-repeat;
	}
	.line a.link:active {
	    background: #386B7F
	}

</style>