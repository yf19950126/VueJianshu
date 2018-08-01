<template>
    <div class="follow">
        <myheader></myheader>
        <div class="content my-container">
            <div class="row">
                <div class="aside">
                    <nuxt-link data-toggle="dropdown" class="change-type" to="allFollow/friend">
                        全部关注
                    </nuxt-link>
                    <!--<ul class="dropdown-menu arrow-top">-->
                        <!--<li>-->
                            <!--<a>全部关注</a>-->
                        <!--</li>-->
                        <!--<li>-->
                            <!--<a>只看作者</a>-->
                        <!--</li>-->
                        <!--<li>-->
                            <!--<a>只看专题</a>-->
                        <!--</li>-->
                        <!--<li>-->
                            <!--<a>只看文集</a>-->
                        <!--</li>-->
                        <!--<li>-->
                            <!--<a>只看推送更新</a>-->
                        <!--</li>-->
                    <!--</ul>-->
                    <nuxt-link to="/follow" class="add-people">
                        <i class="fa fa-user-plus"></i>
                        <span>添加关注</span>
                    </nuxt-link>
                    <ul class="js-subscription-list">
                        <li>
                            <nuxt-link to="/allFollow/friend" class="wrap" active-class="active">
                                <div class="avatar">
                                    <img src="../assets/img/13.png" style="border: none;">
                                </div>
                                <div class="name">简友圈</div>
                            </nuxt-link>
                        </li>
                        <li class="">
                            <nuxt-link to="/allFollow/person" class="wrap" active-class="active">
                                <div class="avatar">
                                    <img src="//upload.jianshu.io/users/upload_avatars/10405676/c9bbb9f1-4762-4d9d-8b63-fe4013dc6618?imageMogr2/auto-orient/strip|imageView2/1/w/120/h/120">
                                </div>
                                <div class="name">奥_f061</div>
                                <span class="count">1</span>
                            </nuxt-link>
                        </li>
                    </ul>
                    <!---->
                    <!---->
                </div>
                <div class="main">
                    <div>
                        <ul class="trigger-menu">
                            <nuxt-link active-class="active" tag="li" to="/follow" exact>
                                <a>全部推荐</a>
                            </nuxt-link>
                            <nuxt-link active-class="active" tag="li" to="/follow/authorRecome">
                                <a>
                                    <i class="fa fa-user"></i>
                                    推荐作者
                                </a>
                            </nuxt-link>
                            <nuxt-link active-class="active" tag="li" to="/follow/specialRecome">
                                <a>
                                    <i class="fa fa-th-large"></i>
                                    推荐专题
                                </a>
                            </nuxt-link>
                        </ul>
                        <nuxt-child/>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
    import myheader from '../components/myHeader'
    export default {
        name: "follow",
        components:{
            myheader
        }
    }
</script>

<style scoped>
    .aside {
        position: fixed;
        top: 0;
        bottom: 0;
        margin: 86px 0 0;
        padding: 0 0 30px;
        width: 280px;
        overflow: auto;
        border-right: 1px solid #f0f0f0;
    }
    .aside .change-type {
        margin-left: 15px;
        font-size: 15px;
    }
    .aside .add-people {
        float: right;
        margin: 4px 10px 0 0;
        font-size: 13px;
        color: #333;
    }
    a {
        cursor: pointer;
    }
    .add-people span {
        margin-left: 4px;
    }
    .aside ul {
        margin-top: 7px;
        list-style: none;
        border-top: 1px solid #f0f0f0;
    }
    ul {
        padding-left: 0;
    }
    ol, ul {
        margin-bottom: 10px;
    }
    li {
        line-height: 20px;
    }
    .aside li:first-child .wrap {
        border-radius: 0 0 0 4px!important;
    }
    .aside .wrap {
        padding: 10px 13px;
        display: block;
    }
    .aside .avatar {
        width: 40px;
        height: 40px;
        margin-right: 4px;
        display: inline-block;
    }
    .avatar img {
        width: 100%;
        height: 100%;
        border-radius: 50%;
    }
    .aside .name {
        font-size: 14px;
        vertical-align: middle;
        display: inline-block;
        max-width: 160px;
        overflow: hidden;
        text-overflow: ellipsis;
        white-space: nowrap;
    }
    .aside .avatar-collection {
        width: 40px;
        height: 40px;
        margin-right: 4px;
        display: inline-block;
    }
    .avatar-collection img {
        width: 100%;
        height: 100%;
        border: 1px solid #ddd;
        border-radius: 10%;
    }
    .aside .count {
        float: right;
        margin-top: 10px;
        font-size: 14px;
        color: #969696;
    }
    .content .row .main{
        padding-left: 0;
        margin-left: 33.333%;
        width: 66.66667%;
        margin-top: 20px;
    }
    .content .row .main div .trigger-menu{
        margin-bottom: 20px;
        border-bottom: 1px solid #f0f0f0;
        font-size: 16px;
        color: #333;
    }
    .content .row .main div .trigger-menu li.active{
        border-bottom: 2px solid #646464!important;
    }
    .content .row .main div .trigger-menu li{
        position: relative;
        display: inline-block;
        padding: 8px 0;
        margin-bottom: -1px;
    }
    .content .row .main div .trigger-menu .active a{
        color: #646464!important;
    }
    .content .row .main div .trigger-menu li a{
        padding: 13px 20px;
        font-size: 15px;
        font-weight: 700;
        color: #969696!important;
        line-height: 25px;
    }
    @media (max-width: 1080px) {
        .content{
            width: 750px!important;
        }
        .aside{
            width: 218.75px;
        }
        .content .row .aside .name{
            max-width: 100px;
        }
    }
    @media (max-width: 750px) {
        .follow{
            overflow: hidden;
        }
    }
</style>