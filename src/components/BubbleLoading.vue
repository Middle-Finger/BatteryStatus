<template>
    <div class="bubble-loading">20%</div>
</template> 

<style>
    .bubble-loading {
        position:relative;
        display:flex;
        justify-content: center;
        align-items: center;
        border-radius: 100%;
        width: 40px;
        height:40px;
        background-image: linear-gradient(45deg, rgb(14,14,46),rgb(64,64,113));
        font-size: 12px;
        font-weight: bold;
        color:white;
        box-shadow: 0 3px 2px 1px rgba(0, 0, 0, 0.2);
    }
        .bubble-loading::before,
        .bubble-loading::after {
            content:'' ;
            position:absolute;
            left:50%;
            top:50%;
            margin-left: -20px;
            margin-top: -20px;
            width:40px;
            height:40px;
            background:rgb(51, 149, 230);
            border-radius: 100%;
            z-index:-1;
            transform: translateY(-2px);
        }
        .bubble-loading::before {
            animation: rotate2 infinite 3s linear;
        }
        .bubble-loading::after {
            animation: rotate2 infinite 2s linear;
        }
        @keyframes rotate2 {
            0% {
                transform: rotate(0deg) translateY(-1.5px);
            }
            100% {
                transform: rotate(360deg) translateY(-1.5px);
            }
        }
</style>