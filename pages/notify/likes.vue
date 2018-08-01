<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<div>
			<div class="menu">收到的喜欢和赞</div>
			<ul class="like-list">
				<li class="">
					<a href="/u/e1dee8bdf974" class="avatar">
                        <img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120">
                    </a>
					<div class="info">
						<a href="/u/e1dee8bdf974" class="user">奥_f061</a>
                        <span>喜欢了你的文章</span>
						<a href="/p/31c472558bc2">《2018-03-02》</a>
						<div class="time">2018.03.02 11:14</div>
					</div>
				</li>
				<div class="notification-list-placeholder" style="display: none;">
					<div class="avatar"></div>
					<div class="wrap">
						<div class="name"></div>
						<div class="text"></div>
					</div>
					<p></p>
					<p class="animation-delay"></p>
					<div class="meta"><i class="iconfont ic-list-comments"></i>
						<div class="text"></div> <i class="iconfont ic-go"></i>
						<div class="text longer"></div>
					</div>
				</div>
			</ul>
			<!---->
			<div>
				<!---->
			</div>
		</div>
	</div>
</template>

<script>
	export default {
		name: "like"
	}
</script>

<style scoped>
    .main {
        padding-left: 0;
    }
    .col-xs-offset-8 {
        margin-left: 33.33333%;
    }
    .col-xs-16 {
        width: 66.66667%;
    }
    .main .menu {
        margin-bottom: 20px;
        font-size: 14px;
        font-weight: 700;
    }
    .main ul {
        list-style: none;
    }
    ul {
        padding-left: 0;
    }
    ol, ul {
        margin-top: 0;
        margin-bottom: 10px;
    }
    .main .like-list li{
        padding: 20px;
        border-top: 1px solid #f0f0f0;
        line-height: 20px;
    }
    .main .like-list .avatar{
        display: inline-block;
        margin-right: 5px;
        width: 40px;
        height: 40px;
    }
    .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 50%;
    }
    .main .like-list .info{
        display: inline-block;
        vertical-align: top;
        width: 535px;
        font-size: 0;
        line-height: 1.7;
    }
    .main .like-list .info .user{
        margin: 0 5px 0 0;
        color: #333!important;
    }
    .main .like-list .info span{
        font-size: 15px;
    }
    .main .like-list .info a{
        font-size: 15px;
        color: #3194d0 !important;
    }
    .main .like-list .time{
        margin-top: 2px;
        font-size: 12px;
        color: #969696;
        line-height: normal;
    }
</style>