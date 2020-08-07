<template>
	<view class="caigou_index">
		<view class="purchaseNote">
			<view class="head">
				<view class="tab_box flex flex_align_center flex_around">
					<view class="tab" :class="{'active': isActive === index}" v-for="(item,index) in list" @click="tabs(item,index)">
						<view>{{item.tab}}</view>
						<view class="xian" v-if="isActive == index"></view>
					</view>
				</view>
			</view>
			<view class="list_box">
				<view class="inp_box flex flex_center" v-if="isActive == 0">
					<view class="left" style="margin-right: 30rpx;">
						<view class="flex flex_center">
							<view class="time">
								<input type="text" v-model="time" placeholder="请选择商品" disabled="true"  @tap="dateVisible1=true"/>
							</view>
							<view class="btn" @click="search()">
								<text class="iconfont iconseach-"></text>
							</view>
						</view>
					</view>
					<view class="right">
						规格：<text>请选择</text>
					</view>
				</view>
				<view class="inp_box flex flex_center" v-if="isActive == 1">
					<view class="left">
						<view class="flex flex_center">
							<view class="time">
								<input class="time_inp" type="text" v-model="time" placeholder="请选择日期" disabled="true"  @tap="dateVisible1=true"/>
							</view>
							<view class="btn" @click="search()">
								<text class="iconfont iconseach-"></text>
							</view>
						</view>
					</view>
				</view>
				
				<view class="record_item" v-if="isActive == 0">
					<view class="record_title">
						近5次采购单价（元）
					</view>
					<view class="item flex flex_center flex_between">
						<view>2020-06-15</view>
						<view class="red_font">¥1.00</view>
					</view>
					<view class="item flex flex_center flex_between">
						<view>2020-06-15</view>
						<view class="red_font">¥1.00</view>
					</view>
				</view>
				
				<view class="enquiry_item" v-if="isActive == 1">
					1
				</view>
				
				
				
			</view>
			
		</view>
		<tabar :tabarIndex="tabNum"></tabar>
	</view>
</template>

<script>
	import tabar from "../../../components/tabbar/caigou.vue"
	const app = getApp().globalData;
	const {
		navBar,
		appid,
		appsecret,
	} = app;
	export default {
		components: {
			tabar
		},
		data() {
			return {
				navBar: navBar,
				isActive: 1,
				tabNum: 3,
				list: [{
						tab: "历史记录",
						id: 1
					},
					{
						tab: "发起询价",
						id: 2
					}
				]
			}
		},
		methods: {
			tabs(item, index) {
				this.isActive = index;
			}

		}
	}
</script>

<style>
	page{
		background-color: #FFFFFF;
	}
	.purchaseNote .head {
		position: fixed;
		width: 100%;
		top: 0;
		left: 0;
		background: #F9F9F9;
	}
	.purchaseNote .tab_box {
		padding: 0 30rpx;
		color: #666666;
		font-family: PingFang SC;
		margin-bottom: 20rpx;
	}

	.purchaseNote .tab_box .tab {
		height: 60rpx;
		line-height: 60rpx;
		padding-bottom: 10rx;
		text-align: center;
	}

	.purchaseNote .tab_box .tab.active {
		color: #03A98E;
	}
	.purchaseNote .tab_box .tab .xian {
		width: 38rpx;
		height: 5rpx;
		background: rgba(3, 169, 142, 1);
		border-radius: 10rpx;
		position: relative;
		left: 50%;
		margin-left: -19rpx;
	}

	.purchaseNote .inp_box {
		background-color: #FFFFFF;
		padding: 15rpx;
		border-bottom: 10rpx solid #F9F9F9;
	}
	.purchaseNote .inp_box .time{
		background-color: #F5F5F5;
		padding: 15rpx 20rpx;
		border-radius: 50rpx 0 0 50rpx;
	}
	.purchaseNote .inp_box .time input{
		width: 350rpx;
		margin-left: 20rpx;
	}
	.purchaseNote .inp_box .time .time_inp{
		width: 550rpx;
	}
	.purchaseNote .inp_box .btn{
		background-color: #03A98E;
		padding: 15rpx 30rpx;
		border-radius: 0 50rpx 50rpx 0;
		color: #FFFFFF;
	}
	.purchaseNote .inp_box .right{
		font-size: 28rpx;
	}
	.purchaseNote .inp_box .right .text{
		color: #666666;
	}	
	.purchaseNote .list_box {
		padding-top: 85rpx;
		padding-bottom: 110rpx;
	}
	.purchaseNote .list_box .record_item {
		padding: 0 20rpx 0 20rpx;
	}
	.purchaseNote .list_box .record_item .item {
		background: #ffffff;
		padding: 10rpx 0;
		font-size: 28rpx;
	}
	.purchaseNote .list_box .record_item .record_title {
		background: #ffffff;
		padding: 15rpx 0;
		border-bottom: 1px solid #F0F0F0;
	}


</style>
