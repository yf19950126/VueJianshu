a
<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<table>
			<thead>
				<tr>
					<th class="setting-head"></th>
					<th></th>
				</tr>
			</thead>
			<tbody class="account">
				<tr>
					<td class="setting-title top-line">打包下载文章</td>
					<td class="top-line">
						<a href="/backup/download" class="btn btn-hollow">下载所有文章</a>
					</td>
				</tr>
			</tbody>
		</table>
		<div class="delete-account-content">
			<a class="show-button" @click="showCount" v-if="disappear">
				删除帐号
                <i class="fa fa-chevron-down"></i>
            </a>
            <transition :duration="200" name="fade">
                <div class="content" v-if="show">
                    <h4>永久删除帐号</h4>
                    <ul>
                        <li>如果你不小心创建出了多余的帐号，或在绑定帐号的时候提示帐号被占用，你可以在
                            <a href="/p/eea64a29cf9d">简书帐号绑定解绑相关问题汇总</a>中获得相关帮助。</li>
                        <li>如果你对简书上的某些内容、功能或社区规则不满意，你可以在
                            <a href="/help">帮助与反馈页</a>向我们提出。</li>
                        <li>删除帐号前，请确保已经没有任何公开或私密文章，且钱包中全部余额已清零。</li>
                        <li>删除帐号是不可逆的操作，删除后将无法恢复。</li>
                    </ul>
                    <a class="btn btn-hollow" @click="saveCount">保留我的帐号</a>
                    <a class="btn btn-delete" @click="deleteCount">删除帐号</a>
                </div>
            </transition>
		</div>
		<!---->
	</div>
</template>
<script>
	export default {
		name: 'misc',
        data(){
		    return{
		        show:false,
                disappear:true
            }
        },
        methods:{
            showCount:function () {
                this.show=true
                this.disappear=false
            },
            saveCount:function () {
                this.show=false
                this.disappear=true
            },
            deleteCount:function () {
                alert("请确认你确实要删除你的账户，此操作无法恢复！")
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
     .main table {
         width: 100%;
     }
     .main tr:last-child {
         border: none;
     }
     .main .setting-title {
         font-size: 15px;
         color: #969696;
     }
      .main .top-line {
         padding-top: 0;
     }
      .main td {
         padding: 20px 0;
     }
     .main .account .btn-delete, .main .account .btn-hollow {
         font-size: 14px;
     }
     .btn-hollow {
         border: 1px solid rgba(59,194,29,.7);
         color: #42c02e!important;
     }
     .btn-delete, .btn-gray, .btn-hollow {
         padding: 4px 12px;
         font-weight: 400;
         line-height: normal;
         border-radius: 40px;
         background: none;
     }
     .btn-hollow:focus, .btn-hollow:hover {
         border: 1px solid #42c02e;
         color: #42c02e!important;
         background-color: rgba(59,194,29,.05);
     }
     .account tr{
         border-bottom: 1px solid #f0f0f0 !important;
     }
      .main .delete-account-content {
         padding-top: 20px;
         border-top: 1px solid #f0f0f0;
     }
      .main .delete-account-content .show-button {
         font-size: 15px;
         color: #969696!important;
     }
     .delete-account-content{
         cursor: pointer;
     }
    .main .delete-account-content .content h4 {
        margin-bottom: 25px;
        font-size: 18px;
        margin-top: 10px;
    }
    .main .delete-account-content .content ul {
       font-size: 14px;
    }
    .main .delete-account-content .content ul li {
        margin-bottom: 15px;
        margin-left: 15px;
    }
    li {
        line-height: 20px;
        list-style-type: disc;
    }
    .main .delete-account-content .content ul li a {
        color: #3194d0;
    }
    a {
        cursor: pointer;
    }
    .main .btn-hollow {
        font-size: 14px;
    }
    .btn-hollow {
        border: 1px solid rgba(59,194,29,.7);
        color: #42c02e!important;
        margin-left: -5px;
    }
    .btn-delete, .btn-gray, .btn-hollow {
        padding: 4px 12px;
        font-weight: 400;
        line-height: normal;
        border-radius: 40px;
        background: none;
    }
     .main .btn-delete, .main .btn-hollow {
        font-size: 14px;
    }
    .btn-delete {
        border: 1px solid rgba(236,97,73,.7);
        color: #ea6f5a!important;
        margin-left: 15px;
    }
</style>
