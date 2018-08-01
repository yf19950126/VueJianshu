<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<div>
			<div class="menu">全部关注</div>
			<ul class="follow-list">
				<li class="">
					<a href="/u/e1dee8bdf974" class="avatar">
                        <img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120"></a>
					<div class="info">
						<a href="/u/e1dee8bdf974" class="user">奥_f061</a> <span>关注了你</span>
						<div class="time">2018.03.01 14:56</div>
					</div>
					<a class="btn btn-default" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
						<i class="fa" :class="iconObj" ref="icon"></i>
						<span ref="followWord">已关注</span>
					</a>
				</li>
				<div class="notification-list-placeholder" style="display: none;">
					<div class="avatar"></div>
					<div class="wrap">
						<div class="btn"></div>
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
		name: "follows",
		data(){
		    return{
                followObj:{
                    'follow':false,
                    'following':true
                },
                iconObj:{
                    'fa-plus':false,
                    'fa-check':true
                },
			}
		},
        methods:{
            isFollow:function(){
                let word = this.$refs.followWord.innerHTML;
				/*这里预留关注的ajax操作*/
                this.followObj.follow = !this.followObj.follow;
                this.followObj.following = !this.followObj.following;
                this.iconObj['fa-plus'] = !this.iconObj['fa-plus'];
                this.iconObj['fa-check'] = !this.iconObj['fa-check'];
                this.$refs.followWord.innerHTML = word == '关注' ? '已关注' : '关注';
            },
            noFollow:function(){
                let word = this.$refs.followWord.innerHTML;
                if(word == '已关注'){
                    this.$refs.followWord.innerHTML = '取消关注';
                    this.$refs.icon.className = 'fa fa-close';
                }
            },
            beFollow:function(){
                let word = this.$refs.followWord.innerHTML;
                if(word == '取消关注'){
                    this.$refs.followWord.innerHTML = '已关注';
                    this.$refs.icon.className = 'fa fa-check';
                }
            },
        }
	}
</script>

<style scoped>
	.follow {
		background:#42c02e;
		color:#ffff!important;
		font-size:12px;
		border-radius: 20px;
		padding:1px 8px 1px 6px;
	}
	.following {
		background:#fff !important;
		color:#969696 !important;
		border:1px solid #ccc;
		font-size:12px;
		border-radius: 20px;
		padding:1px 8px 1px 6px;
	}
	.following:hover{
		background: none !important;
	}
    .main {
        padding-left: 0;
    }
    .col-xs-offset-8 {
        margin-left: 33.33333%;
    }
    .col-xs-16 {
        width: 66.66667%;
    }
    ul {
        list-style: none;
    }
    ul {
        padding-left: 0;
    }
    ol, ul {
        margin-top: 0;
        margin-bottom: 10px;
    }
    .follow-list li{
        padding: 20px;
        border-top: 1px solid #f0f0f0;
    }
    li {
        line-height: 20px;
    }
    .main .follow-list .avatar{
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
    .main .follow-list .info {
        display: inline-block;
        vertical-align: top;
        font-size: 0;
        width: 535px;
        line-height: 1.7;
    }
    .main .follow-list .info {
        max-width: 420px;
    }
    .main .follow-list .info .user{
        margin: 0 5px 0 0;
        color: #333;
        font-size: 15px;
        cursor: pointer;
    }
    .main .follow-list .info span{
        font-size: 15px;
    }
    .follow-list .time{
        margin-top: 2px;
        font-size: 13px;
        color: #969696;
        line-height: normal;
    }
     .main .follow-list .btn {
        padding: 8px 0;
        width: 100px;
        float: right;
        font-size: 15px;
    }
</style>