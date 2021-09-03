#简单的地区三级联动

##使用说明

太懒了直接上代码吧~~

```html
//组件使用示例
<pca-picker-cc v-on:getAddressResultObj="getAddressResultObj" :addressList.sync="addressList">
    <view class="uni-input">{{ addressList.join(' ') }}</view>
</pca-picker-cc>
```

```js
export default {
    data() {
        return {
            //使用了.sync更新自动同步最新地区信息
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
```

以上是使用方式.

##结束语

如有bug,请在评论区提交