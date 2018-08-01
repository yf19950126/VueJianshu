<template>
    <div class="col-xs-16 col-xs-offset-8 main">
        <div>
            <ul class="note-list">
                <li class="">
                    <!---->
                    <div class="content">
                        <div class="author">
                            <a href="/u/e1dee8bdf974"  class="avatar">
                                <img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96">
                            </a>
                            <div class="info">
                                <a href="/u/e1dee8bdf974"  class="nickname">奥_f061</a>
                                <span>喜欢了文章 · 24分钟前</span>
                            </div>
                        </div>
                        <a href="/p/3b4618f77364?utm_source=desktop&amp;utm_medium=timeline"  class="title">
                            <span>只为了显示评论功能</span>
                        </a>
                        <p class="abstract">一只前端。</p>
                        <div class="meta">
                            <div class="origin-author">
                                <a href="/u/f7f63e2dd8f4" >无关所有</a>
                            </div>
                            <a href="/p/3b4618f77364?utm_source=desktop&amp;utm_medium=timeline" >
                                <i class="fa fa-eye"></i> 2
                            </a>
                            <a href="/p/3b4618f77364#comments" >
                                <i class="fa fa-comment"></i> 1
                            </a>
                            <span>
								<i class="fa fa-heart"></i> 1
							</span>
                            <!---->
                        </div>
                    </div>
                </li>
                <li class="">
                    <!---->
                    <div class="content">
                        <div class="author">
                            <a href="/u/e1dee8bdf974"  class="avatar"><img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96"></a>
                            <div class="info">
                                <a href="/u/e1dee8bdf974" class="nickname">奥_f061</a>
                                <span>喜欢了文章 · 4小时前</span>
                            </div>
                        </div>
                        <a href="/p/31c472558bc2?utm_source=desktop&amp;utm_medium=timeline"  class="title">
                            <span>2018-03-02</span>
                        </a>
                        <p class="abstract">德玛西亚</p>
                        <div class="meta">
                            <div class="origin-author">
                                <a href="/u/49d62a85da4c" target="_blank">帆帅无敌</a>
                            </div>
                            <a href="/p/31c472558bc2?utm_source=desktop&amp;utm_medium=timeline">
                                <i class="fa fa-eye"></i> 1</a>
                            <a href="/p/31c472558bc2#comments">
                                <i class="fa fa-comment"></i> 1
                            </a>
                            <span>
								<i class="fa fa-heart"></i> 1
							</span>
                            <!---->
                        </div>
                    </div>
                </li>
                <li class="have-img">
                    <a href="/p/31f532b1329e?utm_source=desktop&amp;utm_medium=timeline"  class="wrap-img"><img src="//upload-images.jianshu.io/upload_images/1359662-3df1c4028637358a?imageMogr2/auto-orient/strip|imageView2/1/w/300/h/240"></a>
                    <div class="content">
                        <div class="author">
                            <a href="/u/e1dee8bdf974"  class="avatar"><img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/96/h/96"></a>
                            <div class="info">
                                <a href="/u/e1dee8bdf974" target="_blank" class="nickname">奥_f061</a>
                                <span>喜欢了文章 · 02.26 15:09</span>
                            </div>
                        </div>
                        <a href="/p/31f532b1329e?utm_source=desktop&amp;utm_medium=timeline" target="_blank" class="title">
                            <span>周日被我射熄火了，所以今天是周一！！！！！</span>
                        </a>
                        <p class="abstract">
                            大家好，我是小丸子，好久不见啦！ 前段时间杭州下大雪，刚好需要搬家，花了好几天时间，
                            现在总算把新家打理好了。这次为了装扮这个新家，我在网上淘了许多高品质的精美小物件，
                            虽然总体...</p>
                        <div class="meta">
                            <div class="origin-author">
                                <a href="/u/24bca2bb387d" target="_blank">小丸子的杂物集</a>
                            </div>
                            <a href="/p/31f532b1329e?utm_source=desktop&amp;utm_medium=timeline" >
                                <i class="fa fa-eye"></i> 21917</a>
                            <a href="/p/31f532b1329e#comments" >
                                <i class="fa fa-comment"></i> 88
                            </a>
                            <span>
								<i class="fa fa-heart"></i> 1450
							</span>
                            <span>
								<i class="fa fa-jpy"></i> 1
							</span>
                        </div>
                    </div>
                </li>
                <!---->
                <a class="load-more">阅读更多</a>
            </ul>
            <!---->
        </div>
    </div>
</template>
<script>
    export default {
        name: 'friend'
    }
</script>
<style scoped>
    .main {
        padding-left: 0;
        margin-top: 30px;
    }
    .col-xs-offset-8 {
        margin-left: 33.33333%;
    }
    .col-xs-16 {
        width: 66.66667%;
    }
    .note-list {
        margin: 0;
        padding: 0;
        list-style: none;
    }
    .note-list li {
        position: relative;
        width: 100%;
        margin: 0 0 17px;
        padding: 0 2px 17px 0;
        border-bottom: 1px solid #f0f0f0;
        word-wrap: break-word;
    }
    .note-list .author {
        margin-bottom: 14px;
        font-size: 13px;
    }
    .note-list .author .avatar, .note-list .author .info {
        display: inline-block;
        vertical-align: middle;
    }
    .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 50%;
    }
    .note-list .author .info .nickname {
        vertical-align: middle;
    }
    .note-list .author a {
        color: #333;
    }
    a {
        cursor: pointer;
    }
    .note-list .author .info span {
        display: inline-block;
        padding-left: 3px;
        color: #969696;
        vertical-align: middle;
    }
    .note-list .title {
        margin: -7px 0 4px;
        display: inherit;
        font-size: 18px;
        font-weight: 700;
        line-height: 1.5;
    }
    .title span:hover{
        border-bottom: 1px solid #333;
    }
    .note-list .abstract {
        margin: 0 0 8px;
        font-size: 13px;
        line-height: 24px;
    }
    .note-list .meta {
        padding-right: 0!important;
        font-size: 12px;
        font-weight: 400;
        line-height: 20px;
    }
    .note-list .origin-author {
        display: inline;
        margin-bottom: 5px;
        font-size: 12px;
        color: #969696;
    }
    .note-list .meta a {
        color: #b4b4b4;
    }
    .note-list .origin-author a:first-child {
        color: #3194d0!important;
    }
    .note-list .meta a {
        margin-right: 10px;
        color: #b4b4b4!important;
    }
    .fa {
        color: #b4b4b4;
    }
    .fa:hover{
        color: #2f2f2f!important;
    }
    .load-more {
        width: 100%;
        height: 40px;
        margin: 30px auto 60px;
        padding: 10px 15px;
        text-align: center;
        font-size: 15px;
        border-radius: 20px;
        color: #fff!important;
        background-color: #a5a5a5;
        display: block;
    }
    .load-more:hover {
        background-color: #969696!important;
    }
</style>