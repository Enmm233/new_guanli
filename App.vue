<script>
	export default {
		//全局共享数据
		globalData: {
			// #ifdef APP-PLUS
			navBar: true,
			// #endif
			// #ifdef MP-WEIXIN |H5
			navBar: false,
			// #endif
			appid: '2',
			appsecret: '123456',
			// #ifdef APP-PLUS |MP-WEIXIN |MP-ALIPAY
			rootUrl: 'https://test.caidj.cn', //主接口地址
			imgRemote: 'https://test.caidj.cn',
			// #endif
			// #ifdef H5
			isWeixin: false,
			rootUrl: '/api', //主接口地址
			// rootUrl: window.location.protocol + "//" + window.location.hostname, //线上地址
			imgRemote: 'http://test.caidj.cn',
			// #endif
		},
		onLaunch: function() {
			console.log('App Launch')
		},
		onShow: function() {
			console.log('App Show')
		},
		onHide: function() {
			console.log('App Hide')
		}
	}
</script>

<style>
	@font-face {font-family: "iconfont";
	  src: url('//at.alicdn.com/t/font_1957858_73887euxs63.eot?t=1596010908958'); /* IE9 */
	  src: url('//at.alicdn.com/t/font_1957858_73887euxs63.eot?t=1596010908958#iefix') format('embedded-opentype'), /* IE6-IE8 */
	  url('data:application/x-font-woff2;charset=utf-8;base64,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') format('woff2'),
	  url('//at.alicdn.com/t/font_1957858_73887euxs63.woff?t=1596010908958') format('woff'),
	  url('//at.alicdn.com/t/font_1957858_73887euxs63.ttf?t=1596010908958') format('truetype'), /* chrome, firefox, opera, Safari, Android, iOS 4.2+ */
	  url('//at.alicdn.com/t/font_1957858_73887euxs63.svg?t=1596010908958#iconfont') format('svg'); /* iOS 4.1- */
	}
	
	.iconfont {
	  font-family: "iconfont" !important;
	  font-size: 16px;
	  font-style: normal;
	  -webkit-font-smoothing: antialiased;
	  -moz-osx-font-smoothing: grayscale;
	}
	
	.iconyou:before {
	  content: "\e64a";
	}
	
	.iconicon-test:before {
	  content: "\e606";
	}
	
	.iconqingniaoxitongtubiao_xia:before {
	  content: "\e66d";
	}
	
	.iconseach-:before {
	  content: "\e677";
	}
	
	.iconcha:before {
	  content: "\e604";
	}
	
	.iconxuanze:before {
	  content: "\e602";
	}
	
	.iconxuanze1:before {
	  content: "\e610";
	}
	
	.iconcart:before {
	  content: "\e737";
	}
	
	.iconicon_jiaoseguanli:before {
	  content: "\e626";
	}
	
	.icontuihuo:before {
	  content: "\e744";
	}
	
	.iconwenti:before {
	  content: "\e608";
	}
	
	.iconzhengyanzhuanhuan:before {
	  content: "\e617";
	}
	
	.iconindex:before {
	  content: "\e65c";
	}
	
	.iconwodezhangdan:before {
	  content: "\e635";
	}
	
	.iconbangdingweixin:before {
	  content: "\e603";
	}
	
	.iconhedui:before {
	  content: "\e688";
	}
	
	.iconmima:before {
	  content: "\e60f";
	}
	
	.iconyanjingbiyan:before {
	  content: "\e61d";
	}
	
	.iconwode:before {
	  content: "\e605";
	}
	
	.iconUserpersonalinform:before {
	  content: "\e600";
	}
	
	.iconxunjia:before {
	  content: "\e613";
	}
	
	.icontuichudenglu:before {
	  content: "\e601";
	}
	page{
		font-family:PingFang SC;
	}
	input{  
		background:none;  
		outline:none;  
		border:none !important;
	}
	input:focus{   
		border:none !important;
	}
	page{
		background: #F9F9FB;
		font-size: 30rpx;
		color: #333333;
	}
	.red_font{
		color: #FF4949;
	}
	.green_font{
		color: #03A98E;
	}
	.uni-navbar--border{
		border: none !important;
	}
	.uni-navbar__header{
		position: fixed !important;
	}
	.uni-input-placeholder{
		color: #C2C2C2;
	}
	.flex{
		display: flex;
	}
	.flex_column{
		display: flex;
		flex-direction: column;
	}
	.flex_center{
		align-items: center;
		justify-content: center;
	}
	.flex_align_center{
		align-items: center;
	}
	.flex_start{
		align-items: flex-start;
	}
	.flex_end{
		align-items: flex-end;
	}
	.flex_around{
		justify-content: space-around;
	}
	.flex_between{
		justify-content: space-between;
	}

</style>
