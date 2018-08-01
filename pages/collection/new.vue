<template>
	<div>
		<my-header></my-header>
		<div class="container new-collection">
			<div class="row">
				<div class="col-xs-18 col-xs-offset-3 main">
					<h3>新建专题</h3>
					<table>
						<thead>
							<tr>
								<th class="setting-head"></th>
								<th></th>
							</tr>
						</thead>
						<tbody class="base">
							<tr>
								<td>
									<div class="avatar-collection">
                                        <img src="../../assets/img/15.png">
                                    </div>
								</td>
								<td>
									<a rel="noreferrer" class="btn btn-hollow">
                                        <input unselectable="on" type="file" class="hide">
                                        上传专题封面
									</a>
								</td>
							</tr>
							<tr>
								<td class="setting-title">名称</td>
								<td>
                                    <input class="nickname" type="text" name="nick-name" placeholder="填写名称，不超过50字">
                                </td>
							</tr>
							<tr>
								<td class="setting-title pull-left setting-input">描述</td>
								<td>
                                    <textarea placeholder="填写描述"></textarea>
                                </td>
							</tr>
							<tr class="add-manager">
								<td class="setting-title pull-left setting-input">其他管理员</td>
								<td>
									<div class="user-add"><input type="text" name="nick-name" placeholder="输入用户名" data-toggle="dropdown">
										<ul class="dropdown-menu"></ul>
									</div>
								</td>
							</tr>
							<tr>
								<td class="setting-title setting-verticle">是否允许投稿</td>
								<td>
									<div class="col-xs-6">
                                        <input type="radio" name="push" value="true" @click="disable">
                                        <span>允许</span>
                                    </div>
									<div class="col-xs-18">
                                        <input type="radio" name="push" value="false" @click="able">
                                        <span>不允许</span>
                                    </div>
								</td>
							</tr>
							<tr :class="{disabled:disabled}">
								<td class="setting-title setting-verticle">投稿是否需要审核</td>
								<td>
									<div class="col-xs-6">
                                        <input type="radio" name="verify" value="true" disabled="disabled">
                                        <span>需要</span>
                                    </div>
									<div class="col-xs-18">
                                        <input type="radio" name="verify" value="false" disabled="disabled">
                                        <span>不需要</span>
                                    </div>
								</td>
							</tr>
						</tbody>
					</table>
					<div class="btn btn-success follow create">创建专题</div>
				</div>
			</div>
		</div>
	</div>
</template>
<script>
	import myHeader from "../../components/myHeader.vue"
	export default {
		name: "new",
		components: {
			myHeader
		},
		data(){
		    return{
		        disabled:false
            }
        },
        methods:{
		    able:function () {
                this.disabled = true
            },
            disable:function () {
                this.disabled = false
            }
        }
	}
</script>
<style scoped>
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
    @media (max-width: 770px) {
        .new-collection .main td {
            display: block;
            width: calc(100vw - 50px);
        }
        .container{
            margin: 0!important;
        }
        .main {
            margin: 0 !important;
        }
    }

    .container {
        width: 960px;
		margin-right: auto;
		margin-left: auto;
		padding-left: 15px;
		padding-right: 15px;
	}
	.new-collection .row {
		padding-top: 30px;
		margin-left: -15px;
		margin-right: -15px;
	}
    .new-collection .main {
        margin-bottom: 60px;
    }
    .col-xs-offset-3 {
        margin-left: 12.5%;
    }
    .col-xs-18 {
        width: 75%;
    }
    .new-collection .main h3 {
        margin: 10px 0 20px;
        font-size: 21px;
        font-weight: 700;
        color: #333;
    }
    .new-collection .main table {
        width: 100%;
        background-color: transparent;
        border-collapse: collapse;
        display: table;
    }
    thead {
        display: table-header-group;
        vertical-align: middle;
        border-color: inherit;
    }
    tr {
        display: table-row;
        vertical-align: inherit;
        border-color: inherit;
    }
    td, th {
        display: table-cell;
        vertical-align: inherit;
    }
    .new-collection .main .setting-head {
        width: 150px;
    }
    tbody {
        display: table-row-group;
        vertical-align: middle;
        border-color: inherit;
    }
    .new-collection .main td {
        padding: 16px 0;
        font-size: 15px;
    }
    .new-collection .main .avatar-collection {
        cursor: default;
        width: 100px;
        height: 100px;
    }
    .new-collection .main .btn-hollow {
        font-size: 14px;
        border: 1px solid rgba(59,194,29,.7);
        color: #42c02e!important;
        padding: 4px 12px;
        font-size: 12px;
        font-weight: 400;
        line-height: normal;
        border-radius: 40px;
        background: none;
    }
    .new-collection .main .hide {
        position: absolute;
        display: block!important;
        width: 82px;
        opacity: 0;
    }
    .new-collection .main input {
        padding: 10px 15px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
    }
    .new-collection .main .setting-title {
        font-size: 15px;
        color: #969696;
    }
    .new-collection .main input[name=nick-name] {
        width: 100%;
    }
    .new-collection .main input {
        padding: 10px 15px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
    }
    .new-collection .main .setting-input {
        line-height: 33px;
    }
    .new-collection .main .setting-title {
        font-size: 15px;
        color: #969696;
    }
    .new-collection .main textarea {
        width: 100%;
        height: 100px;
        margin-bottom: 10px;
        padding: 10px 15px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
        display: block;
        resize: none;
        outline-style: none;
    }
    .new-collection .main .setting-title {
        font-size: 15px;
        color: #969696;
    }
    .col-xs-6 {
        width: 25%;
        float: left;
        position: relative;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
    }
    input[type=checkbox], input[type=radio] {
        margin: 4px 0 0;
        line-height: normal;
        box-sizing: border-box;
    }
    .new-collection .main span {
        margin: 0 5px 0 10px;
        font-size: 15px;
        color: #333;
        vertical-align: middle;
    }
    .col-xs-18 {
        width: 75%;
        min-height: 1px;
        padding-left: 15px;
        padding-right: 15px;
    }
    .new-collection .main input {
        padding: 10px 15px;
        font-size: 15px;
        border: 1px solid #c8c8c8;
        border-radius: 4px;
        background-color: hsla(0,0%,71%,.1);
    }
    .new-collection .main span {
        margin: 0 5px 0 10px;
        font-size: 15px;
        color: #333;
        vertical-align: middle;
    }
    .new-collection .main .create {
        margin: 20px 0 50px;
        border-radius: 20px;
    }
    .follow {
        border-color: #42c02e;
        padding: 8px 22px;
        font-size: 16px;
        font-weight: 400;
        line-height: normal;
    }
    .disabled td,.disabled span{
        color: lightgray!important;
    }
</style>