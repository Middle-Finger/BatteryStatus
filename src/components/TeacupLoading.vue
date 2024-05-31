<template>
    <div class="teacup-loading">20%</div>
</template>

<style>
    .teacup-loading {
        position:  relative;
        display: flex;
        justify-content: center;
        border: 4px solid rgb(30, 29, 20);
        border-radius: 0 0 16px 16px;
        border-top-width: 0;
        width: 40px;
        height: 40px;
        background-color: #fff3da;
        font-size: 10px;
        font-weight:bold;
        line-height: 24px ;
        color: rgb(30, 29, 20);
        overflow: hiddern;
        box-shadow:0 1px 2px 1px rgba(0, 0, 0, 0.2);
        transform: translateZ(0);
    }
    .teacup-loading::before,
    .teacup-loading::after {
        content: '';
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 0;
        right: -120px;
        height: 20px;
       
    }
    .teacup-loading::before {
        background-color: rgb(255, 214, 125);
         
    }
    .teacup-loading::after {
        background-color: rgb(255, 174, 0);
       
    }
   

</style>