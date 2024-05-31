<template>
    <view class="battery-loading">
        <view class="conver"></view>
    </view>
</template>
<style>
.battery-loading{
    position: relative;
    display: flex;
    justify-content: center;
    align-items:center;
    width:200px;
    height:280px;
    bottom: 10px;
    background-color: white;
    border-radius: 15px 15px 5px 5px;
}
.battery-loading::before{
    content: '';
    position: absolute;
    top:-20px;
    left: 37%;
    width: 50px;
    height: 20px;
    background-color: white;
    border-radius: 5px  5px 0 0;
}
.battery-loading::after{
    content: '';
    position: absolute;
    left: 0;
    right: 0;
    bottom: 0;
    background-image: linear-gradient(to bottom,#57fa72 0%, #51ea6b 44%, #4CD964 100%);
    animation: charge 10s linear infinite;
}
@keyframes charge{
    0%{
        top:100%;
        filter:hue-rotate(40deg);
    }
    95%{
        top:5%;
        border-radius: 0px;
    }
    100%{
        top:0%;
        border-radius: 15px 15px 0 0;
    }
}
    .conver{
		width: 100%;
		height: 100%;
		position: absolute;
		left: 0;
		top: 0;
		border-radius: 15px 15px 5px 5px;
		z-index: 1;
	
        overflow: hidden;
	}
    /*两个伪元素通用的样式*/
    .conver::before,
	.conver::after{
		content: '';
		position: absolute;
		left: -50%;
		width: 400px;
		height: 400px;
	}
    /*分别设置两个伪元素不同的背景色透明度和边框圆角*/
	.conver::before{
		background-color: rgba(255,255,255,1);
		border-radius: 40% 30%;
        /*添加动效*/
		animation: rotate1 10s linear infinite;
	}
	.conver::after{
		background-color: rgba(255,255,255,0.7);
		border-radius: 50% 40%;
        /*添加动效*/
		animation: rotate2 10s linear infinite;
	}
@keyframes rotate1{
		0%{
			transform: rotate(30deg);
			bottom: -8%;
		}
		100%{
			transform: rotate(270deg);
			bottom: 100%;
		}
	}
	@keyframes rotate2{
		0%{
			transform: rotate(45deg);
			bottom: -6%;
		}
		100%{
			transform: rotate(360deg);
			bottom: 95%;
		}
	}
</style>