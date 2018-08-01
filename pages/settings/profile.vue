<template>
	<div class="col-xs-16 col-xs-offset-8 main">
		<table>
			<thead>
				<tr>
					<th class="setting-head"></th>
					<th></th>
				</tr>
			</thead>
			<tbody class="information">
				<tr>
					<td class="top-line setting-title setting-verticle">
						性别
					</td>
					<td class="top-line">
                        <input type="radio" value="1" name="nan">
                        <span>男</span>
                        <input type="radio" value="2" name="nan">
                        <span>女</span>
                        <input type="radio" value="0" name="nan">
                        <span>保密</span>
                    </td>
				</tr>
				<tr>
					<td class="setting-title pull-left">个人简介</td>
					<td>
						<form>
                            <textarea placeholder="填写你的个人简介"></textarea>
                        </form>
					</td>
				</tr>
				<tr>
					<td class="setting-title pull-left setting-input">个人网站</td>
					<td>
						<form>
                            <input type="text" name="website" placeholder="http://你的网址">
							<p class="pull-right">填写后会在个人主页显示图标</p>
						</form>
					</td>
				</tr>
				<tr>
					<td class="setting-title">微信二维码</td>
					<td class="weixin-qrcode">
                        <input type="file" class="hide">
						<a class="btn btn-hollow">
                            <input type="file" class="hide"> 更换图片
						</a>
						<p class="pull-right">上传后会在个人主页显示图标</p>
					</td>
				</tr>
				<tr>
					<td class="setting-title setting-input pull-left">社交帐号</td>
					<td class="social-bind">
						<p>你可以通过绑定的社交帐号登录简书。出于安全因素, 你最初用来创建账户的社交帐号不能移除。</p>
						<p>如果帐号被占用，你可以在
							<a href="/p/eea64a29cf9d">简书帐号绑定解绑相关问题汇总</a>
                            中获得相关帮助。
                        </p>
						<ul class="social-bind-list">
							<li>
								<div class="bind-name">
                                    <i class="fa fa-weibo"></i>
									<a href="/users/auth/weibo">
                                        绑定微博
                                        <i class="fa fa-chevron-right"></i>
                                    </a>
								</div>
							</li>
							<li>
								<div class="bind-name">
                                    <i class="fa fa-weixin"></i>
									<a href="/users/auth/wechat">
                                        绑定微信
                                        <i class="fa fa-chevron-right"></i>
                                    </a>
								</div>
							</li>
							<li>
								<div class="bind-name">
                                    <i class="fa fa-qq"></i>
									<a href="/users/auth/qq_connect">
                                        绑定 QQ
                                        <i class="fa fa-chevron-right"></i>
                                    </a>
								</div>
							</li>
							<li>
								<div class="bind-name">
                                    <i class="fa fa-leaf"></i>
									<a href="/users/auth/douban">
                                        绑定豆瓣
                                        <i class="fa fa-chevron-right"></i>
                                    </a>
								</div>
							</li>
							<li>
								<div class="bind-name">
                                    <i class="fa fa-google"></i>
									<a href="/users/auth/google_oauth2">
                                        绑定 Google+
                                        <i class="fa fa-chevron-right"></i></a>
								</div>
							</li>
						</ul>
					</td>
				</tr>
			</tbody>
		</table>
        <input type="submit" class="btn btn-success setting-save" value="保存">
    </div>
</template>
<script>
	export default {
		name: 'profile'
	}
</script>
<style scoped="">
    .main tr:first-child {
        border: none;
    }
	.main {
		padding-left: 0;
	}
	
	.col-xs-offset-8 {
		margin-left: 33.333333%;
	}
	
	.col-xs-16 {
		width: 66.66667%;
		padding-right: 15px;
	}
	
	.main table {
		width: 100%;
	}
	.information tr:first-child{
		border-bottom: 1px solid #f0f0f0;
	}
	table {
		background-color: transparent;
		border-collapse: collapse;
		border-spacing: 0;
	}
	
	tbody {
		display: table-row-group;
		vertical-align: middle;
		border-color: inherit;
	}
	
	.main tr {
		border-bottom: 1px solid #f0f0f0;
	}
	
	.main .setting-verticle {
		vertical-align: bottom;
	}
	
	.main .setting-title {
		font-size: 15px;
		color: #969696;
	}
	
	.main .top-line {
		padding-top: 0;
	}
	
	.main td {
		padding: 20px 10px;
	}
	
	input[type=checkbox],
	input[type=radio] {
		margin: 4px 0 0;
		line-height: normal;
		box-sizing: border-box;
		padding: 0;
	}
	
	.main span {
		margin: 0 20px 0 6px;
		font-size: 15px;
		vertical-align: middle;
	}
	
	.main textarea {
		width: 100%;
		height: 100px;
		margin-bottom: 10px;
		padding: 8px 10px;
		font-size: 15px;
		border: 1px solid #c8c8c8;
		border-radius: 4px;
		background-color: hsla(0, 0%, 71%, .1);
		display: block;
		resize: none;
		outline-style: none;
	}
	
	.main form {
		margin: 0;
	}
	
	.main .information input[name=website] {
		width: 100%;
		margin-bottom: 10px;
	}
	
	.main input[type=email],
	.main input[type=text] {
		padding: 5px 10px;
		font-size: 15px;
		border: 1px solid #c8c8c8;
		border-radius: 4px;
		background-color: hsla(0, 0%, 71%, .1);
	}
	
	.main p {
		margin: 0;
		padding: 8px 0 0;
		font-size: 12px;
		color: #969696;
		clear: both;
	}
	
	.pull-right {
		float: right!important;
	}
	
	.main .btn-delete,
	.main .btn-hollow {
		font-size: 14px;
	}
	
	.btn-hollow {
		border: 1px solid rgba(59, 194, 29, .7);
		color: #42c02e!important;
	}
	
	.btn-delete,
	.btn-gray,
	.btn-hollow {
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
	.main .hide {
		position: absolute;
		display: block!important;
		width: 82px;
		opacity: 0;
	}
	
	.main .information .social-bind {
		padding-bottom: 10px;
	}
	
	.main p a {
		color: #3194d0;
	}
	
	.main .information .social-bind-list {
		margin: 0;
		list-style: none;
	}
	
	ul {
		padding-left: 0;
	}
	
	.main .information .social-bind-list li {
		border-bottom: 1px solid #f0f0f0;
		line-height: 50px;
		font-size: 0;
	}
	
	.main .information .social-bind-list .bind-name {
		display: inline-block;
	}
	
	.main .information .social-bind-list i {
		width: 30px;
		font-size: 20px;
		vertical-align: middle;
		display: inline-block;
	}
	
	.main .information .social-bind-list .bind-name a {
		margin: 0 0 0 20px;
		font-size: 14px;
		vertical-align: middle;
	}
	
	.main .setting-save {
		width: 100px;
		margin: 30px 0 60px;
		border-radius: 20px;
		border: none;
	}
    .fa-weibo{
        color: #e05244;
    }
    .fa-weixin{
        color: #00bb29;
    }
    .fa-qq{
        color: lightskyblue;
    }
    .fa-leaf{
        color: #42c02e;
    }
    .fa-google{
        color: #ea6f5a!important;
    }
    .fa-chevron-right{
        color: #333!important;
        font-size: 5px !important;
        font-style: normal !important;
		margin-left: 10px;
		width: 30px;
    }
</style>