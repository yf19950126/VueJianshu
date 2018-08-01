<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<div>
			<div class="menu">收到的评论</div>
			<ul class="comment-list">
				<li class="">
					<a href="/u/e1dee8bdf974" class="avatar"><img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120"></a>
					<div class="info">
						<div>
							<a class="user" href="/u/e1dee8bdf974">奥_f061</a>
							<span class="comment-slogan">评论了你的文章</span>
							<a href="/p/31c472558bc2">《2018-03-02》</a>
						</div>
						<div class="time">2018.03.02 11:13</div>
					</div>
					<p>无敌</p>
					<div class="meta">
						<a class="function-btn" @click="showForm">
							<i class="fa fa-comment-o"></i>
							<span>回复</span>
						</a>
						<a href="/p/31c472558bc2#comment-21163298" class="function-btn">
							<i class="fa fa-hand-o-right"></i>
							<span>查看对话</span>
						</a>
					</div>
					<div>
                        <transition :duration="200" name="fade">
                            <form class="new-comment" v-if="show">
                                <!----><textarea placeholder="写下你的评论..."></textarea>
                                <div class="write-function-block">
                                    <div data-v-b36e9416="" class="emoji-modal-wrap">
                                        <a data-v-b36e9416="" class="emoji">
                                            <i data-v-b36e9416="" class="fa fa-smile-o"></i>
                                        </a>
                                        <!---->
                                    </div>
                                    <div class="hint">Ctrl+Enter 发表</div>
                                    <a class="btn btn-send" @click="show=false">发送</a>
                                    <a class="cancel" @click="show=false">取消</a>
                                </div>
                            </form>
                        </transition>
					</div>
				</li>
				<div class="notification-list-placeholder comment" style="display: none;">
					<div class="avatar"></div>
					<div class="wrap">
						<div class="name"></div>
						<div class="text"></div>
					</div>
					<p></p>
					<p class="animation-delay"></p>
					<div class="meta">
						<i class="iconfont ic-list-comments"></i>
						<div class="text"></div>
						<i class="iconfont ic-go"></i>
						<div class="text longer"></div>
					</div>
				</div>
			</ul>
			<!---->
			<div>
				<!---->
			</div>
			<!---->
		</div>
	</div>
</template>

<script>
	export default {
		name: "comments",
		data() {
			return {
                show:false,
			}
		},
		methods: {
            showForm:function () {
                this.show = !this.show
            },
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
	ol,
	ul {
		margin-top: 0;
		margin-bottom: 10px;
	}
	.main .comment-list li {
        padding: 20px;
        border-top: 1px solid #f0f0f0;
    }
	.main .comment-list .avatar {
		display: inline-block;
		margin-right: 5px;
		width: 40px;
		height: 40px;
	}
    .function-btn{
         cursor: pointer;
     }
	.avatar img {
		width: 100%;
		height: 100%;
		border: 1px solid #ddd;
		border-radius: 50%;
	}
	.main .comment-list .info {
		display: inline-block;
		vertical-align: top;
		width: 535px;
		font-size: 0;
		line-height: 1.7;
	}
	.main .comment-list .info .user {
		margin: 0 5px 0 0;
		color: #333!important;
        cursor: pointer;
	}
	.main .comment-list .info .comment-slogan {
		font-size: 15px;
		color: #333;
	}
	.main .comment-list .info a {
		font-size: 15px;
		color: #3194d0 !important;
		cursor: pointer;
	}
	.main .comment-list .time {
		margin-top: 2px;
		font-size: 12px;
		color: #969696;
		line-height: normal;
	}
	.main .comment-list p {
		margin: 10px 0 0;
		font-size: 15px;
		line-height: 1.7;
	}
	.main .comment-list .meta {
		margin-top: 10px;
		height: 20px;
	}
	.main .comment-list .meta .function-btn {
		float: left;
		margin-right: 30px;
		font-size: 13px;
		color: #969696!important;
	}
    .main .comment-list .meta .function-btn:hover {
        color: #333!important;
    }
	.fa {
		margin-right: 8px;
		font-size: 16px;
	}
	.main .new-comment {
		margin: 20px 0 0;
	}
    .main .new-comment textarea {
        padding: 10px 15px;
        width: 100%;
        height: 80px;
        font-size: 13px;
        border: 1px solid #dcdcdc;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
        resize: none;
        display: inline-block;
        vertical-align: top;
        outline-style: none;
    }
    .new-comment .write-function-block {
        height: 50px;
    }
    .main .new-comment .emoji i {
        font-size: 20px;
        color: #969696;
    }
    .main .new-comment .hint {
        float: left;
        margin: 20px 0 0 20px;
        font-size: 13px;
        color: #969696;
    }
    .main .new-comment .btn-send {
        float: right;
        width: 78px;
        margin: 10px 0;
        padding: 8px 18px;
        font-size: 16px;
        border: none;
        border-radius: 20px;
        color: #fff!important;
        background-color: #42c02e;
        cursor: pointer;
        outline: none;
        display: block;
    }
    .main .new-comment .cancel {
        float: right;
        margin: 18px 30px 0 0;
        font-size: 16px;
        color: #969696!important;
        cursor: pointer;
    }
    .main .new-comment .cancel:hover{
        color: #333!important;
    }
    .emoji-modal-wrap[data-v-b36e9416] {
        position: relative;
    }
    .main .new-comment .emoji {
        float: left;
        margin: 19px 0 0;
    }
</style>