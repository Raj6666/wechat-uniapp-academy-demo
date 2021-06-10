<template>
    <view class="wrapper">
        <image src="../static/images/home-banner.png" class="banner"/>
        <view class="detail-wrapper">
            乐学书院
        </view>
        <view class="box-wrapper">
            <view class="box-item">
                <view class="title">师资团队</view>
                <image src="../static/images/box1.png"/>
            </view>
            <view class="box-item">
                <view class="title">品牌介绍</view>
                <image src="../static/images/box1.png"/>
            </view>
        </view>
        <view class="gallery-wrapper">
            <view class="header"><span>教学风采</span><span>更多</span></view>
            <view class="gallery">
                <Gallery :imgList="imgList"></Gallery>
            </view>
        </view>
    </view>
</template>
<script>
import Gallery from '../components/gallery'
export default {
		data() {
			return {
				title: '测试',
                imgList: []
			}
		},
        components: {
			Gallery
		},
		onLoad() {
            this.imgList = [
                'http://img.alicdn.com/bao/uploaded/i4/2324043857/O1CN016lc9XZ1eMYIsRsz53_!!2324043857.jpg',
                'https://img1.vvic.com/upload/1621613176323_925327.jpg',
                'https://img1.vvic.com/upload/1621613198761_612228.jpg',
                'https://img1.vvic.com/upload/1621613203005_467302.jpg',
            ]
		},
		methods: {

		}
	}
</script>
<style lang="scss" scoped>
    .wrapper {
        position: relative;
        display: flex;
        flex-direction: column;
        width: 100vw;
        .banner {
            width: 100%;
            height: 516rpx;
        }
        .detail-wrapper {
            position: absolute;
            top: 422rpx;
            left: 50%;
            transform: translateX(-50%);
            height: 252rpx;
            width: calc(100vw - 46rpx);
            background-color: #fff;
            border-radius: 15px;
            padding: 10rpx;
            box-sizing: border-box;
            box-shadow: rgb(189, 189, 189) 0px 0px 10rpx;
        }
        .box-wrapper {
            width: 100%;
            height: 154rpx;
            margin-top: 200rpx;
            display: flex;
            justify-content: space-around;
            padding: 0 16rpx;
            box-sizing: border-box;
            .box-item {
                width: 48%;
                position: relative;
                border-radius: 15px;
                overflow: hidden;
                box-shadow: rgb(189, 189, 189) 0px 0px 10rpx;
                .title {
                    position: absolute;
                    top: 25rpx;
                    left: 10rpx;
                }
                image {
                    width: 100%;
                    height: 100%;
                }
            }
        }
        .gallery-wrapper {
            display: flex;
            flex-direction: column;
            margin-top: 60rpx;
            padding: 0 23rpx;
            .header {
                display: flex;
                justify-content: space-between;
                align-items: center;
                span:nth-child(1) {
                    font-size: 32rpx;
                    font-weight: bold;
                }
                span:nth-child(2) {
                    color: rgb(183, 183, 183);
                }
            }
            .gallery {
                height: 380rpx;
            }
        }
    }
</style>