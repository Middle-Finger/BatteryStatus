<template>
    <div class="circle-loading">20%</div>
</template>

<style>
    .circle-loading{
        position: relative;
        display: flex;
        justify-content:center ;
        align-items: center;
        border:4px solid rgb(184, 187, 191);
        border-radius: 100%;
        width:40px;
        height:40px;
        font-size: 12px;
        font-weight: bold;
        color:rgb#07fe14;
        box-shadow: 0 1px 2px 1px rgba(0,0,0, 0.2),
        inset 0 1px 2px 1px rgba(0,0,0, 0.2);
    }
    .circle-loading::before {
        content: '';
        position: absolute;
        left: 50%;
        top: 50%;
        margin-left: -24px;
        margin-top: -24px;
        display: block;
        border:4px solid transparent;
        border-top-color:#f78fb3;
        border-radius: 100%;
        width:40px;
        height: 40px;
        animation: rotate1 infinite 2s ease;
    }
    @keyframes rotate1 {
        0% {
            transform: rotate(0deg);
        }
        100%{
            transform: rotate(360deg);
        }
    }
</style>