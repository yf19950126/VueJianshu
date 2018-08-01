<template>
	<div class="news-container">
		<myheader></myheader>
		<div class="content my-container">
			<div class="row">
				<div class="aside">
					<ul>
						<li>
							<nuxt-link active-class="active" to="/settings/basic" exact>
								<i class="fa fa-list"></i>
								<span>基础设置</span>
							</nuxt-link>
						</li>
						<li>
							<nuxt-link active-class="active" to="/settings/profile">
								<i class="fa fa-envelope-open-o"></i>
								<span>个人资料</span>
							</nuxt-link>
						</li>
						<li>
							<nuxt-link active-class="active" to="/settings/misc">
								<i class="fa fa-cog"></i>
								<span>账号管理</span>
							</nuxt-link>
						</li>
					</ul>
				</div>
				<nuxt-child/>
			</div>
		</div>
	</div>
</template>

<script>
    import myheader from '../components/myHeader'
    export default {
        name: "settings",
        components:{
            myheader
        }
    }
</script>

<style scoped>
	.content{
		width: 960px!important;
		margin: 0 auto!important;
		padding: 0 15px;
	}
	.content .row{
		padding: 30px 0;
		margin: 0 -15px;
	}
	.content .row .aside{
		position: fixed;
		top: 0;
		bottom: 0;
		margin: 86px 0 0;
		padding: 0 0 30px;
		width: 280px;
		overflow: auto;
	}
	.content .row .aside ul{
		margin-top: 0;
		margin-bottom: 10px;
	}
	.content .row .aside ul li{
		line-height: 20px;
		margin: 0;
		color: #333;
	}
	.content .row .aside ul li a{
		height: auto;
		padding: 15px 25px;
		display: block;
		font-size: 15px;
	}
	.content .row .aside ul li a:hover{
		background-color: #f0f0f0;
		border-radius: 4px;
	}
	.content .row .aside ul li a i{
		width: 30px;
		height: 30px;
		text-align: center;
		color: white;
		line-height: 30px;
		margin-right: 15px;
		font-size: 20px;
		background-color: #969696;
		vertical-align: middle;
	}
	.content .row .aside ul li a span{
		font-size: 15px;
		vertical-align: middle;
	}
	.content .row .aside ul li a.active {
		background-color: #f0f0f0 !important;
		border-radius: 4px;
	}

	@media (max-width: 1080px) {
		.content{
			width: 750px!important;
		}
		.aside{
			width: 218.75px!important;
		}
	}
	@media (max-width: 750px) {
		.news-container{
			overflow: hidden;
		}
	}
</style>