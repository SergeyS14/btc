<script>
import IconBase from './common/IconBase.vue';
import IconApple from './common/IconApple.vue';
import IconAndroid from './common/IconAndroid.vue';
import IconWin from './common/IconWin.vue';
import IconLinux from './common/IconLinux.vue'

export default{
    components:{IconBase, IconApple, IconAndroid, IconWin, IconLinux}
}

</script>
<template>
    <div class="container">
    <div class="dow">
        <div>
        <span class="dow__title">
            Кошелек и Инструменты
        </span>
        <p class="dow__text">
            BTCA предоставляет вам инструменты и ресурсы, чтобы вы всегда могли контролировать свои средства.
        </p>
        <div class="dow__svg">
            <icon-base class="svgs" width="37" height="37" icon-name="Android"><icon-android /></icon-base>
            <icon-base class="svgs" width="37" height="37" icon-name="Apple"><icon-apple /></icon-base>
            <icon-base class="svgs" width="37" height="37" icon-name="Linux"><icon-linux /></icon-base>
            <icon-base class="svgs" width="32" height="32" icon-name="Win"><icon-win /></icon-base>
        </div>
        <button class="dow__btn">
            <icon-base class="dow__btn__svg" width="32" height="32" icon-name="Apple"><icon-apple /></icon-base>
            Скачать кошелек
        </button>
    </div>
        <div class="device">
            <img class="device__mac" src="../assets/images/ScreenMac.png"/>
            <img class="device__border" src="../assets/images/iPhone 12 border.png"/>
            <img class="device__iphone" src="../assets/images/iphoneScreen.png"/>
        </div>
    </div>
</div>
</template>
<style lang="scss">

.dow{
    margin: 0;
    width: 42rem;
    display: flex;
    padding-top: 12.7rem;
    &__title{
        @include text(h1);
        background: linear-gradient(91.92deg, #FFFFFF 29.24%, rgba(176, 250, 255, 0) 131.64%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;
        width: 35.1rem;
        

    }
    &__text{
        @include text(text);
        color: white;
        width: 42rem;
        
    }
    &__svg{
        display: flex;
        gap: 24px;
        margin-top: 4rem;
        margin-bottom: 3.2rem;
    }
    &__btn{
        width: 22.6rem;
        height: 5.2rem;
        @include text(button);
        padding-left: 2.4rem;
        padding-right: 2.4rem;
        padding-top: 1.4rem;
        padding-bottom: 1.4rem;
        text-align: center;
        display: flex;
        color: #8886FF;
        border-radius: 1.2rem;
        background-color: #627FE326 ;
        border: none;
        cursor: pointer;

      
        &__svg{
            width: 2rem;
            height: 2.4rem;
            padding-left: .4rem;
            padding-bottom: .4rem;
            margin-right: 1.6rem;
            color: #8886FF;

            
        }
    }
}

.svgs{
    width: 3.2rem;
    height: 3.2rem;
    color: #636D85;
}

.device{
    position: relative;
    margin-left: 3rem;
    &__mac{
        background: #000;
        padding: 1.7rem;
        border-radius: 1.7rem;

    }
    &__border{
        z-index:1 ;
        position: absolute;
        left: 44rem;
        bottom: .1rem
        

    }
    &__iphone{
        z-index:2;
        position: absolute;
        left: 45.2rem;
        border-radius: 3rem;
        bottom: 1rem;
        
    }
}

</style>