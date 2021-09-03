<template>
	<view>
		<page-head title="地区三级联动demo"></page-head>

		<!-- #ifndef MP-ALIPAY -->
		<view class="uni-title uni-common-pl">地区选择器</view>
		<view class="uni-list">
			<view class="uni-list-cell">
				<view class="uni-list-cell-left">
					当前选择
				</view>
				<view class="uni-list-cell-db">
					<pca-picker-cc v-on:getAddressResultObj="getAddressResultObj" :addressList.sync="addressList">
						<view class="uni-input">{{ addressList.join(' ') }}</view>
					</pca-picker-cc>
				</view>
			</view>
		</view>
		<!-- #endif -->
	</view>
</template>
<script>
	export default {
		data() {
			return {
				addressList: ["广东省", "深圳市", "南山区"],
			}
		},
		methods: {
			getAddressResultObj(e){
        //获取详细的 省/市/区 对象信息,更新时被动调,主动调用请自行设置ref值,方法一致
			  console.log(e)
			},
		}
	}
</script>

<style>
.uni-picker-tips {
	font-size: 12px;
	color: #666;
	margin-bottom: 15px;
	padding: 0 15px;
	/* text-align: right; */
}
</style>
