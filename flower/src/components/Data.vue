<template>
	<div>
		<ul class="datas">
			<li :class="{default : status === 0, selected : status === 1, disable : status === 2}">123</li>
		</ul>
	</div>	
</template>

<script>
	export default {
		data () {
			return {
				 status:0
			}
		},
		methods:{

		}
	}
</script>

<style>
	.datas>li{
		float: left;
		list-style: none;
		width: 150px;
		height: 80px;
		box-sizing: border-box;
		text-align: center;
		padding: 15px 0;
		border: 1px solid #ccc;
	}
	.default{
		background: #fff;
		color: #000;
	}
	.selected{
		background: #ff4c44;
		color: #fff;
	}
	.disable{
		background: #f2f2f2;
	}
</style>