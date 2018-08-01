<template>
    <div>
        <my-header></my-header>
        <div class="person my-container">
            <div class="row">
                <div class="col-8 main">
                    <div class="main-top">
                        <nuxt-link class="avatar" to="/u/123">
                            <img src="../../assets/img/fanshuai.jpg">
                        </nuxt-link>
                        <button class="off user-follow-button"  :class="followObj" @click="isFollow" @mouseover="noFollow" @mouseleave="beFollow">
                            <i class="fa" :class="iconObj" ref="icon"></i>
                            <span ref="followWord">关注</span>
                        </button>
                        <a class="btn btn-hollow" href="/notifications">
                            发简信
                        </a>
                        <div class="title">
                            <nuxt-link class="name" to="/u/123">
                                帆帅666
                            </nuxt-link>
                            <i class="fa fa-mars"></i>
                        </div>
                        <div class="info">
                            <ul>
                                <li>
                                    <div class="meta-block">
                                        <nuxt-link to="/users/123/following">
                                            <p>88</p>
                                            关注
                                            <i class="fa fa-angle-right"></i>
                                        </nuxt-link>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <nuxt-link to="/users/123/followers">
                                            <p>16</p>
                                            粉丝
                                            <i class="fa fa-angle-right"></i>
                                        </nuxt-link>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <nuxt-link to="/u/123">
                                            <p>32</p>
                                            文章
                                            <i class="fa fa-angle-right"></i>
                                        </nuxt-link>
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <p>5000</p>
                                        字数
                                    </div>
                                </li>
                                <li>
                                    <div class="meta-block">
                                        <p>100</p>
                                        收获喜欢
                                    </div>
                                </li>
                            </ul>
                        </div>
                    </div>
                    <ul class="trigger-menu">
                        <li :class="{active:currentTab == 'MyArticle'}">
                            <a href="javascript:void(0)" @click="toggleTab('MyArticle')">
                                <i class="fa fa-edit"></i>
                                文章
                            </a>
                        </li>
                        <li :class="{active:currentTab == 'MyNew'}">
                            <a href="javascript:void(0)" @click="toggleTab('MyNew')">
                                <i class="fa fa-bell"></i>
                                动态
                            </a>
                        </li>
                        <li :class="{active:currentTab == 'MyComment'}">
                            <a href="javascript:void(0)" @click="toggleTab('MyComment')">
                                <i class="fa fa-compress"></i>
                                最新评论
                            </a>
                        </li>
                        <li :class="{active:currentTab == 'MyHot'}">
                            <a href="javascript:void(0)" @click="toggleTab('MyHot')">
                                <i class="fa fa-fire"></i>
                                热门
                            </a>
                        </li>
                    </ul>
                    <div id="list-container">
                        <!--动态组件-->
                        <component :is="currentTab" keep-alive></component>
                    </div>
                </div>
                <div class="col-4 aside">
                    <div class="title">个人介绍</div>
                    <a class="function-btn"  href="javascript:void(0)" @click="edit">
                        <i class="fa fa-pencil-square-o"></i> 编辑
                    </a>
                    <transition :duration="200" name="fade">
                        <form v-if="show">
                            <textarea></textarea>
                            <a class="btn btn-send" href="javascript:void(0)">
                                发送
                            </a>
                            <a class="cancel" href="javascript:void(0)" @click="cancel">
                                取消
                            </a>
                        </form>
                    </transition>
                    <div class="description" style="display: none">
                        <div class="js-intro">
                            逃跑医生，预防医学专家，抗衰老顾问，创业者，奶爸！人生意义思考者，东方智慧践行者。非著名作家坯子。
                        </div>
                    </div>
                    <ul class="list user-dynamic">
                        <li>
                            <nuxt-link to="/users/123/collection">
                                <i class="fa fa-book"></i>
                                <span>他关注的专题/文集</span>
                            </nuxt-link>
                        </li>
                        <li>
                            <nuxt-link to="/users/123/like">
                                <i class="fa fa-heart-o"></i>
                                <span>他喜欢的文章</span>
                            </nuxt-link>
                        </li>
                    </ul>
                    <div>
                        <!--创建的专题-->
                        <div class="title">
                            他创建的专题
                        </div>
                        <nuxt-link to="/collection/new" class="function-btn new-collection-btn">
                            <i class="fa fa-plus"></i><span>新建专题</span>
                        </nuxt-link>
                        <ul class="list">
                            <li>
                                <nuxt-link to="/collection/123" class="avatar-collection">
                                    <img src="~assets/img/movie.jpg">
                                </nuxt-link>
                                <nuxt-link to="/collection/123" class="name">
                                    朱焘源值班报告
                                </nuxt-link>
                            </li>
                        </ul>
                        <!--管理的专题-->
                        <div class="title">
                            他管理的专题
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link to="/collection/123" class="avatar-collection">
                                    <img src="~assets/img/movie.jpg">
                                </nuxt-link>
                                <nuxt-link to="/collection/123" class="name">
                                    朱焘源值班报告
                                </nuxt-link>
                            </li>
                        </ul>
                        <!--创建的文集-->
                        <div class="title">
                            他创建的文集
                        </div>
                        <ul class="list">
                            <li>
                                <nuxt-link to="/note/123" class="avatar-collection">
                                    <i class="fa fa-book"></i>
                                </nuxt-link>
                                <nuxt-link to="/note/123" class="name">
                                    朱焘源值班报告
                                </nuxt-link>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
    import myHeader from '~/components/myHeader'
    import MyArticle from '@/components/user/MyArticle'
    import MyNew from '@/components/user/MyNew'
    import MyComment from '@/components/user/MyComment'
    import MyHot from '@/components/user/MyHot'
    export default {
        name:'',
        data () {
            return {
                currentTab:'MyArticle',
                followObj:{
                    'follow':true,
                    'following':false
                },
                iconObj:{
                    'fa-plus':true,
                    'fa-check':false
                },
                show:false,
                disappear:true
            }
        },
        methods:{
            toggleTab:function(tab){
                this.currentTab = tab;
            },
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
            edit:function () {
                this.show = true
//                this.disappear = false
            },
            cancel:function () {
                this.show = false
//                this.disappear = true
            }
        },
        components:{
            myHeader,
            MyArticle,
            MyNew,
            MyHot,
            MyComment
        }
    }
</script>
<style scoped="">
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
    textarea{
        margin-bottom: 5px;
        width: 100%;
        height: 125px;
        padding: 5px 10px;
        font-size: 14px;
        background-color: hsla(0,0%,71%,.1);
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        resize: none;
        outline: none;
        /*text-indent: 2em;*/
    }
    .cancel {
        margin-left: 10px;
        font-size: 14px;
        color: #969696 !important;
        line-height: 34px;
        vertical-align: middle;
    }
    .cancel:hover {
        color:#333!important;
    }
    .btn-send {
        padding:5px 20px;
        font-size:14px;
        margin-bottom: 8px;
        border: 1px solid #42c02e;
        border-radius: 20px;
        color:#42c02e!important;
        box-shadow: none;
    }
    .btn-send:hover {
        background:rgb(245,252,243);
    }
</style>