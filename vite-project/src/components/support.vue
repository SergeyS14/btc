<script>
import IconBase from './common/IconBase.vue';
import IconSwap from './common/IconSwap.vue';
export default{
    components:{IconBase, IconSwap}
}
</script>
<template>
<div class="support">
    
<div class="support__content">
        <span class="support__title">Нас поддерживают</span>
        <p class="support__text">Получите свободу, благодаря конфиденциальным, глобальным цифровым деньгам. Становитесь своим собственным банком с полным контролем над своими цифровыми активами.</p>
            <div class="swap">
                <div class="swap__item">
                    <p class="swap__tag">TIPS</p>
                    <p class="swap__text">Swap to see more</p>
                </div>
                <div class="swap__svg">
                    <icon-base width="37" height="37" icon-name="Swap"><icon-swap /></icon-base>
                </div>
            </div>
    </div>
    <p class="bgword">ПАРТНЕРЫ</p>
</div>
</template>
<style lang="scss">
    .support{
        background: rgb(15, 15, 15);
    width: 100%;
    height: 61.7rem;
    position: absolute;
        .bgword{
            position: relative;
            font-family: golos;
            top: -410px;
            left: -32px;
            font-size: 18rem;
            font-weight: 700;
            color: white;
            background: linear-gradient(91.92deg, rgba(255, 255, 255, 0.05) 29.24%, rgba(176, 250, 255, 0) 131.64%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            
        }
        &__content{
            margin-top: 16.8rem;
            margin-left: 16.5rem;
        }
        &__title{
            @include text(h2);
            background: linear-gradient(91.92deg, #FFFFFF 29.24%, rgba(176, 250, 255, 0) 131.64%);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;

        }
        &__text{
            @include text(text);
            color: white;
            width: 56.7rem;
        }
    }

    .swap{
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 49.3rem;
        height: 7.2rem;
        border-radius: 0.8rem;
        background: #151822;

        &__item{
            padding-left: 1.3rem;
        }
        
        &__tag{
            color: white;
            width: 6.8rem;
            height: 2.6rem;
            border-radius: 3.7rem;
            background: #1A204A;
            @include text(small);
            text-align: center;
            line-height: 25px;
            margin: 0px;
            margin-bottom: 0.5rem;
        }
        &__text{
            color: white;
            @include text(text);
            margin: 0px;
            
        }
        &__svg {
           width: 37px;
           height: 37px;
           margin-right: 1.6rem;
        }
    }
    
</style>