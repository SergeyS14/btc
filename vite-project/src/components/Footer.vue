<script>
import IconBase from './common/IconBase.vue';
import IconApple from './common/IconApple.vue';
import IconAndroid from './common/IconAndroid.vue';
import IconWin from './common/IconWin.vue';
import IconLinux from './common/IconLinux.vue'

import IconFace from './common/IconFace.vue'
import IconTwit from './common/IconTwit.vue'
import IconIg from './common/IconIg.vue'
import IconYt from './common/IconYt.vue'
import IconGit from './common/IconGit.vue'

export default{
    components:{IconBase, IconApple, IconAndroid, IconWin, IconLinux, IconFace, IconTwit, IconIg, IconYt, IconGit}
}
</script>
<template>
<div style="background-color: black;">
    <div class="footer container">
        <nav class="footer__nav">
            <ul class="footer__list">
                <p class="footer__title">BTCA</p>
                <li class="footer__item">Продвинутый Proof of Stake</li>
                <li class="footer__item">Холодный стекинг</li>
                <li class="footer__item">Конфиденциальность Shield</li>
                <li class="footer__item">Загрузки</li>
                <li class="footer__item">Мастерноды</li>
                <li class="footer__item">Мерчанты</li>
                <li class="footer__item">Биржи</li>
            </ul>
        </nav>
        <nav class="footer__nav">
            <ul class="footer__list">
                <p class="footer__title">Ресурсы</p>
                <li class="footer__item">Новости</li>
                <li class="footer__item">Десктоп Приложение</li>
                <li class="footer__item">Мобильное Приложение</li>
            </ul>
        </nav>
        <nav class="footer__nav">
            <ul class="footer__list">
                <p class="footer__title">Саппорт</p>
                <li class="footer__item">FAQ</li>
                <li class="footer__item">Саппорт</li>
                <li class="footer__item">Комьюнити</li>
                <li class="footer__item">Почему BTCA</li>
                <li class="footer__item">O BTCA</li>
            </ul>
        </nav>
        <nav class="footer__nav">
            <ul class="footer__list">
                <p class="footer__title">Документация</p>
                <li class="footer__item">Документы</li>
                <li class="footer__item">Terms of Use</li>
                <li class="footer__item">Privacy Policy</li>
                <li class="footer__item">Legal Notices</li>
            </ul>
        </nav>
        <div class="discript">
            <div class="discript__ref">
                <div>
                    <icon-base class="svg" width="37" height="37" icon-name="Android"><icon-android /></icon-base>
                    <icon-base class="svg" width="37" height="37" icon-name="Apple"><icon-apple /></icon-base>
                    <icon-base class="svg" width="37" height="37" icon-name="Linux"><icon-linux /></icon-base>
                    <icon-base class="svg" width="32" height="32" icon-name="Win"><icon-win /></icon-base>
                </div>
                <p class="discript__text">BTCA - это децентрализованная, одноранговая валюта с открытым исходным кодом, отличающаяся расширенными функциями конфиденциальности</p>
            
            </div>
            <div class="discript__svg">
                <icon-base class="svgb"   width="3rem" height="3rem " icon-name="Face"><icon-face /></icon-base>
                <icon-base class="svgb" width="3rem" height="3rem" icon-name="Twit"><icon-twit /></icon-base>
                <icon-base class="svgb" width="3rem" height="3rem" icon-name="Ig"><icon-ig /></icon-base>
                <icon-base class="svgb" width="3rem" height="3rem" icon-name="Yt"><icon-yt /></icon-base>
                <icon-base class="svgb" width="3rem" height="3rem" icon-name="Git"><icon-git /></icon-base>
            </div>
        </div>
        
    </div>
    <div class="discript__line"></div>
    <div class="sub container">
        <p class="sub__text">© 2019-2021 BTCA Community & BTCA Foundation</p>
        <p class="sub__text">Created by BTCA Community</p>
    </div>
</div>
</template>
<style lang="scss">



.footer{
    display: flex;
    padding-top: 4.4rem;
    height: 45rem;

    &__nav{
        width: 20rem;
        height: 22rem;
        
    }
    &__list{
        list-style-type: none;
        @include text(small);
        color: white;
        
        
    }
    &__title{
        margin-bottom: 3.2rem;
        @include text(caption);
        color: white;
        margin-top: 0;
        
    }
    &__item{
        margin-bottom: 1.8rem;
    }
}

.svg{
    width: 2rem;
    height: 2rem;
    color: #636D85;
    margin-right: 1.4rem;

}

.svgb{
    width: 3rem;
    height: 3rem;
    margin-right: 1.4rem;
    background: gray;
    border-radius: 2rem;
    padding-left: .6rem;
    padding-top: .6rem;
    
   
}

.discript{
    margin-top: 2rem;
    margin-left: 6.6rem;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    margin-bottom: 1.2rem;
    &__ref{
        
    }
    &__text{
        width: 29.1rem;
        color: white;
        @include text(small);
        margin-top: 3.2rem;
    }
    &__svg{
        
    }
    &__line{
        border-top: 1px solid #0D111B
    }
}

.sub{
    display: flex;
    justify-content: space-between;

    &__text{
        @include text(small);
        color: white;
        
    }
}
</style>