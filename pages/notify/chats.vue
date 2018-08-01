<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<div>
			<div class="menu">全部简信</div>
			<ul class="jianxin-list">
				<li>
					<div class="pull-right"><span class="time">03.01 14:57</span>
						<div class="open">
							<a data-toggle="dropdown" href="javascript:void(0);" @click="showDrop">
                                <i class="fa fa-chevron-down"></i>
                            </a>
							<transition :duration="200" name="fade">
								<ul class="dropdown-menu" v-if="show">
									<li>
										<a>
											<i class="fa fa-trash-o"></i>删除会话
										</a>
									</li>
									<li>
										<a>
											<i class="fa fa-ban"></i>加入黑名单
										</a>
									</li>
									<li>
										<a class="report">
                                        <span>
                                            <i class="fa fa-flag-o"></i>举报用户
                                        </span>
										</a>
									</li>
								</ul>
							</transition>
						</div>
					</div>
					<a href="/u/e1dee8bdf974" class="avatar">
                        <img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/144/h/144">
						<!---->
					</a>
					<a href="/u/e1dee8bdf974"class="name">奥_f061</a>
					<a href="/notifications/#/chats/664346195" class="wrap">
						<p>阿萨德阿萨德阿萨德撒的散搭打</p>
					</a>
				</li>
				<li>
					<div class="pull-right">
						<span class="time">01.26 16:37</span>
						<div class="open">
							<a data-toggle="dropdown" href="javascript:void(0);" @click="showDropOne">
                                <i class="fa fa-chevron-down"></i>
                            </a>
							<transition :duration="200" name="fade">
								<ul class="dropdown-menu" v-if="showOne">
									<li>
										<a>
											<i class="fa fa-trash-o"></i>删除会话
										</a>
									</li>
									<li>
										<a>
											<i class="fa fa-ban"></i>加入黑名单
										</a>
									</li>
									<li>
										<a class="report">
                                        <span>
                                            <i class="fa fa-flag-o"></i>举报用户
                                        </span>
										</a>
									</li>
								</ul>
							</transition>
						</div>
					</div>
					<a href="/u/b52ff888fd17" class="avatar"><img src="//upload.jianshu.io/users/upload_avatars/3678149/b8a58e70-1126-48c9-97e2-8f21a31dfa94.png?imageMogr2/auto-orient/strip|imageView2/1/w/144/h/144">
						<!---->
					</a>
					<a href="/u/b52ff888fd17" class="name">简宝玉</a>
					<a href="/notifications/#/chats/481248492" class="wrap">
						<p> 欢迎加入丰富多彩的原创内容社区—简书。新手有关简书的任何疑问请点击链接查看 http://w...</p>
					</a>
				</li>
				<!--<div class="jianxin-placeholder" style="display: none;">-->
					<!--<div class="avatar"></div>-->
					<!--<div class="wrap">-->
						<!--<div class="time"></div>-->
						<!--<div class="name"></div>-->
						<!--<div class="text"></div>-->
					<!--</div>-->
				<!--</div>-->
			</ul>
			<!---->
			<!---->
			<!---->
		</div>
	</div>
</template>

<script>
	export default {
		name: "chats",
        data(){
		    return{
				show:false,
				showOne:false
            }
        },
		methods:{
            showDrop:function () {
				this.show = !this.show
            },
            showDropOne:function () {
                this.showOne = !this.showOne
            }
		}
	}
</script>
<style scoped>
	.fade-enter-active,.fade-leave-active {
		opacity: 1;
		transition: .3s;
		-webkit-transition: .3s
	}
	.fade-enter,.fade-leave-to {
		opacity: 0;
		transform: translate3d(0,-5%,0);
		-webkit-transform: translate3d(0,-5%,0);
		transition: .3s;
		-webkit-transition: .3s
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
     .main .jianxin-list .pull-right .time {
        color: #9b9b9b;
    }
    .main .jianxin-list .pull-right div {
        display: inline;
        color: #969696!important;
        margin-left: 5px;
    }
    .main .jianxin-list li {
        position: relative;
        border-top: 1px solid #f0f0f0;
    }
    li {
        line-height: 20px;
        display: list-item;
        text-align: -webkit-match-parent;
    }
    .main .jianxin-list .pull-right {
        margin: 20px 20px 0 0;
        font-size: 13px;
    }
    .pull-right {
        float: right!important;
    }
    .main .jianxin-list .avatar {
        float: left;
        margin: 20px 10px 20px 20px;
        width: 48px;
        height: 48px;
    }
    .avatar {
        display: block;
        cursor: pointer;
    }
     .main .jianxin-list .name {
        position: absolute;
        top: 25px;
        font-size: 15px;
    }
    .main .jianxin-list .wrap {
        display: block;
        padding: 20px 20px 20px 0;
        min-height: 88px;
    }
    a {
        cursor: pointer;
    }
    .main .jianxin-list p {
        margin: 28px 0 0;
        font-size: 12px;
        color: #999;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
	.dropdown-menu {
        top: auto;
        left: auto;
        color: #333;
        min-width: inherit;
		border-color: transparent;
		box-shadow: 0 2px 8px rgba(0,0,0,.1);
		position: absolute;
		z-index: 1000;
		float: left;
		margin-left: -50px;
		padding: 5px 0;
		list-style: none;
		font-size: 14px;
		text-align: left;
		background-color: #fff;
		border-radius: 4px;
		background-clip: padding-box
    }
	.open>.dropdown-menu {
		display: block;
	}
    .dropdown-menu li {
        border: none!important;
    }
	.dropdown-menu li:hover {
		background-color: #eee!important;
	}
     .main .jianxin-list li {
        position: relative;
    }
    .main .jianxin-list .dropdown-menu a {
        padding: 10px 20px;
    }
    .dropdown-menu>li>a {
        display: block;
        clear: both;
        font-weight: 400;
        line-height: 1.42857;
        color: #2f2f2f!important;
        white-space: nowrap;
    }
	.fa{
		margin-right: 10px;
		font-size: 16px;
		color: #969696!important;
	}
</style>