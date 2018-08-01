<template>
    <div>
        <div id="list-container">
            <ul class="user-list" infinite-scroll-url="/users/49d62a85da4c/following" data-placeholder="user">
                <li>
                    <a class="avatar" href="/u/52600243a9d6">
                        <img src="../../assets/img/8.jpg" alt="180">
                    </a>
                    <div class="info">
                        <a class="name" href="/u/52600243a9d6">奥_f061</a>
                        <div class="meta">
                            <span>关注 1</span><span>粉丝 1</span><span>文章 0</span>
                        </div>
                        <div class="meta">
                            写了 0 字，获得了 0 个喜欢
                        </div>
                    </div>
                    <a class="btn btn-default" :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                        <i class="fa" :class="iconObj" ref="icon"></i>
                        <span ref="followWord">已关注</span>
                    </a>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
    export default {
        name: 'MyFollowing',
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
    .person .main .user-list {
        list-style: none;
        clear: both;
    }
    ul {
        padding-left: 0;
    }
    .person .main .user-list li:first-child {
        padding-top: 0!important;
    }
    .person .main .user-list li {
        padding-bottom: 20px;
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        line-height: normal;
    }
    .avatar img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 50%;
    }
    .person .main .user-list .info a, .person .main .user-list .name {
        font-size: 15px;
        font-weight: 700;
        color: #333;
    }
    .person .main .user-list .meta {
        padding-top: 2px;
        font-size: 12px;
        color: #969696;
    }
    .person .main .user-list .meta span {
        margin-right: 10px;
        padding-right: 10px;
        border-right: 1px solid #969696;
    }
    .person .main .user-list .meta {
        padding-top: 2px;
        font-size: 12px;
        color: #969696;
    }
</style>