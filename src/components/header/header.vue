<template>
	<div class="container">
		<div class="bg"></div>
		<div class="content-wrapper">
			<div class="avatar">
				<img  width="64" height="64"src="http://static.galileo.xiaojukeji.com/static/tms/seller_avatar_256px.jpg">
			</div>
			<div class="content">
				<div class="title">
					<span class="brand">
						<img src="./temp.jpg" alt="">
					</span>
					<span class="name">name</span>
				</div>
				<div class="description">description</div>
				<div class="support">
					<span class="icon">
						<img src="./temp.jpg" alt="">
					</span>
					<span class="text">这是数据，等会添加,判断是否显示</span>
				</div>
					
			</div>
		</div>
			
		<div class="bulletin-wrapper">
			<img src="./temp.jpg" alt="">
			<span>这也是数据</span>
		</div>
	</div>
</template>
<script>
	export default{
		data() {
			return {
				seller: {}
			};
		},
		created() {
			this.$http({
				methos:'get',
				url:'api/seller'
				
			}).then(res => {
				
				this.seller = res.data.data;
				
			},res => {
				alert('err');
			})
		},
		methods:{
			
		},
		computed:{},
		components:{}
	}
</script>
<style scoped>
	.container{
		position: absolute;
		left: 0;
		top: 0;
		width:100%;
		height:25%;
		color: #fff;
		
		
	}
	.container .bg{
		width: 100%;
		height: 100%;
		background-repeat: no-repeat;
		background-size: cover;
		background-image: url(http://static.galileo.xiaojukeji.com/static/tms/seller_avatar_256px.jpg);
		filter: blur(4px);
	}
	.content-wrapper{
		position: absolute;
		width: 80%;
		height:80%;
		left: 10%;
		top: 10%;
		
		
	}
	.content-wrapper .content .title{
		position: absolute;
		
		top: 0%;
		width: 192px;
		height:15px;
		margin-left: 80px;
		width: 192px;
		height:15px;
		margin-left: 80px;
		line-height: 15px;
		font-size: 14px;
		width: 192px;
		height:15px;
		margin-left: 80px;
		
	}
	.content-wrapper .content .title .brand img{
		
	}
	.content-wrapper .content .title .name{

		
	}
	.content-wrapper .content .description{
	
		position: absolute;
		left: 33%;
		top: 20%;
		font-size: 14px;
		margin-left: 16px;
	}
	.content-wrapper .content .support{
	
		text-align: left;
		position: absolute;
		width: 192px;
		height:15px;
		top: 47%;
		font-size: 10px;
		margin-left: 80px;
	}
	.bulletin-wrapper{
		
		
		position: absolute;
		width: 80%;
		height:16%;
		left: 10%;
		bottom: 10%;
		
	}
		
	
</style>
