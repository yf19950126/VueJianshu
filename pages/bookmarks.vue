<template>
	<div>
		<my-header></my-header>
		<div class="container bookmarks" id="js-page-top">
			<div class="row">
				<div class="col-xs-18 col-xs-offset-3 main">
					<img class="tag-banner" src="../assets/img/6.png" alt="Collect note">
					<!-- 文章列表模块 -->
					<ul class="note-list">
						<li id="note-24217954" data-note-id="24217954" class="have-img">
							<a class="wrap-img" href="/p/a86be546860e" target="_blank">
								<img class="img-blur-done" src="http://upload-images.jianshu.io/upload_images/7922648-9f51bb3b5cdb4ecd.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240" alt="120">
							</a>
							<div class="content" @mouseenter="show=true" @mouseleave="show=false">
								<div class="author">
									<a class="avatar" target="_blank" href="/u/18f79251b0ac">
										<img src="http://upload.jianshu.io/users/upload_avatars/7922648/bae992e9-14ac-460f-b836-86bf7a4745f4.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64" alt="64">
									</a>
									<div class="info">
										<a class="nickname" target="_blank" href="/u/18f79251b0ac">梁七十一</a>
										<span class="time" data-shared-at="2018-02-23T18:21:46+08:00">02.23 18:21</span>
									</div>
								</div>
								<a class="title" target="_blank" href="/p/a86be546860e">姥爷是阴阳师，姥姥是食人鬼</a>
								<p class="abstract">
									姥爷是阴阳师，他治愈了很多的疑难杂症，帮助很多人的家庭幸福和睦。而他和姥姥，一个死于癌症晚期，一个死于不治之症。他的家族也同他一样没落了...人们说他得罪了神明…… 1 这是...
								</p>
								<div class="meta">

									<a target="_blank" href="/p/a86be546860e">
										<i class="fa fa-eye"></i> 1850
									</a>
									<a target="_blank" href="/p/a86be546860e#comments">
										<i class="fa fa-comment"></i> 82
									</a> <span><i class="fa fa-heart"></i> 47</span>
									<a class="cancel" v-if="show">取消收藏</a>
								</div>
							</div>
						</li>
						<li id="note-24197970" data-note-id="24197970" class="have-img">
							<a class="wrap-img" href="/p/a102289f6834" target="_blank">
								<img class="  img-blur-done" src="http://upload-images.jianshu.io/upload_images/1835526-4306fe275390c832.jpg?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240" alt="120">
							</a>
							<div class="content" @mouseenter="showone=true" @mouseleave="showone=false">
								<div class="author">
									<a class="avatar" target="_blank" href="/u/55b597320c4e">
										<img src="http://upload.jianshu.io/users/upload_avatars/1835526/6ac158c7-6af2-415a-886e-2868dd256783.png?imageMogr2/auto-orient/strip|imageView2/1/w/64/h/64" alt="64">
									</a>
									<div class="info">
										<a class="nickname" target="_blank" href="/u/55b597320c4e">简书出版</a>
										<a target="_blank" href="http://www.jianshu.com/p/fbdc9fc74f0a">
											<img width="30" height="30" class="badge-icon" data-toggle="tooltip" title="" src="../assets/img/7.png" data-original-title="简书员工">
										</a> <span class="time" data-shared-at="2018-02-22T11:13:42+08:00">02.22 11:13</span>
									</div>
								</div>
								<a class="title" target="_blank" href="/p/a102289f6834">朋友们，版君回来了</a>
								<p class="abstract">
									版君今天开始上班了，春节期间，除了个别紧要的评论和简信外，真的一个都没回，也没有收到传说中的夺命连环call，谢谢大家放我过了一个放飞自我的假期_(:зゝ∠)_ 然后现在的未...
								</p>
								<div class="meta">
									<a target="_blank" href="/p/a86be546860e">
										<i class="fa fa-eye"></i> 1850
									</a>
									<a target="_blank" href="/p/a86be546860e#comments">
										<i class="fa fa-comment"></i> 82
									</a>
									<span><i class="fa fa-heart"></i> 47</span>
									<a class="cancel" v-if="showone">取消收藏</a>
								</div>
							</div>
						</li>

					</ul>
				</div>
			</div>
			<div>
				<div>
					<!---->
				</div>
			</div>
			<div class="side-tool">
				<ul>
					<li data-placement="left" data-toggle="tooltip" data-container="body" data-original-title="回到顶部" style="display: none;">
						<a class="function-button"><i class="iconfont ic-backtop"></i></a>
					</li>
					<!---->
					<!---->
					<!---->
					<!---->
				</ul>
			</div>
		</div>
	</div>
</template>
<script>
	import myHeader from '../components/myHeader'
	export default {
		components: {
			myHeader
		},
		data(){
		    return{
                show:false,
				showone:false
			}
		}

	}
</script>
<style scoped>
	@media (max-width: 1080px) {
		.recommend-banner, .tag-banner {
			min-height: 78px;
			border-radius: 4px;
		}
	}
	@media (min-width: 992px) {
		.container {
			width: 960px;
		}
	}
	@media (min-width: 1081px) {
		.container {
			width: 960px;
		}
	}
	@media (min-width: 992px) {
		.container {
			width: 970px;
		}
	}
	@media (min-width: 768px) {
		.container {
			width: 750px;
		}
	}
	.container {
		width: 700px;
		margin-right: auto;
		margin-left: auto;
		padding-left: 15px;
		padding-right: 15px;
	}
	.bookmarks .row {
		padding-top: 30px;
		margin-left: -15px;
		margin-right: -15px;
	}
	.tag-banner {
		margin-bottom: 30px;
		width: 100%;
		min-height: 100px;
		background-color: hsla(0,0%,71%,.2);
		border-radius: 6px;
	}
	img {
		vertical-align: middle;
		border: 0;
	}
	.note-list .have-img>div {
		padding-right: 160px;
	}
	.note-list .title:visited {
		color: #969696;
	}
	.note-list .author {
		margin-bottom: 14px;
		font-size: 13px;
	}
	.note-list .title {
		margin: -7px 0 4px;
		display: inherit;
		font-size: 18px;
		font-weight: 700;
		line-height: 1.5;
		color: #969696!important;
	}
	.note-list .abstract {
		margin: 0 0 8px;
		font-size: 13px;
		line-height: 24px;
	}
	.note-list .have-img .wrap-img img {
		width: 100%;
		height: 100%;
		border-radius: 4px;
		border: 1px solid #f0f0f0;
	}
	.note-list .author .info .badge-icon {
		width: 15px;
		height: 15px;
	}
	.note-list .meta a {
		margin-right: 10px;
		color: #b4b4b4!important;
	}
	.note-list .meta a:hover{
		color: #333!important;
	}
</style>