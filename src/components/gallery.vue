<template>
    <view class="swapper-wrapper">
        <swiper class="swiper" :indicator-dots="indicatorDots" :autoplay="autoplay" :interval="interval" :duration="duration">
            <swiper-item v-for="(item, index) in imgList" :key="index">
                <view class="swiper-item">
                    <view class="page-txt">{{index + 1}}/{{imgList.length}}</view>
                    <image :src="item" alt=""/>
                </view>
            </swiper-item>
        </swiper>
    </view>
</template>
<script>
export default {
     data() {
        return {
            indicatorDots: false,
            autoplay: false,
            interval: 2000,
            duration: 500
        }
    },
    props: {
        imgList: {
            type: Array,
            default: []
        }
    }
}
</script>
<style lang="scss">
    .swapper-wrapper {
        width: 100%;
        height: 100%;
        .swiper-item {
            position: relative;
            height: 100%;
            width: 100%;
            border-radius: 10px;
            overflow: hidden;
            .page-txt {
                position: absolute;
                right: 20rpx;
                bottom: 20rpx;
                color: #fff;
                background-color:rgba(0, 0, 0, 0.4);
                padding: 5rpx 10rpx;
                border-radius: 10px;
            }
            image {
                width: 100%;
	            height: 100%;
            }
        }
    }
</style>