<script>
</script>
<template>
<div style="background-color: black;">
    <div class="start ">
            <span class="start__title">Готовы начать?</span>
            <p class="start__text">Независимо от того, являетесь ли вы разработчиком, мерчантом, конечным пользователем или покупателем окон, мы приветствуем вас в сообществе BTCA.</p>
            <p class="bgword">Ready?</p>
        </div>
        
        
    <div class="step container">
            <article class="step__content">
                <div style="display: flex;">
                    <p class="step__text">1 шаг </p> <div class="step__line"></div>
                </div>
                <span class="step__title">Скачайте приложение</span>
                <img src="../assets/images/hand1.png" class="step__imgO">
            </article>
            <article class="step__content">
                <div style="display: flex;">
                    <p class="step__text">2 шаг </p> <div class="step__line"></div>
                </div>
                <span class="step__title">Регестрируйтесь</span>
                <img src="../assets/images/hand2.png" class="step__imgTw">
            </article>
            <article class="step__content">
                <div style="display: flex;">
                    <p class="step__text">3 шаг </p> <div class="step__line"></div>
                </div>
                <span class="step__title">Пользуйтесь</span>
                <img src="../assets/images/hand3.png" class="step__imgTr">
            </article>
    </div>
    <div class="container">
    <div class="form ">
        <span class="form__title">Никогда не пропускайте обновления</span>
        <p class="form__text">Подпишитесь на информационный бюллетень и будьте первым, кто получит новейшие оповещения, объявления и обновления о разработках BTCA.</p>
        <form class="form__form">
            <input class="form__input" placeholder="Ваш e-mail" type="text" id="email">
            <button class="form__btn">Подписаться</button>
        </form>
    </div>
</div>
    </div>

</template>
<style lang="scss">


.form{
    background-image: url(../assets/images/Rectangle.png);
    width: 114rem;
    height: 40.2rem;
    border-radius: 2.8rem;
    padding-top: 7.5rem;
    padding-left: 5.4rem;

    &__title{
        @include text(h2);
        background: linear-gradient(91.92deg, #FFFFFF 29.24%, rgba(176, 250, 255, 0) 186.24%);
        -webkit-background-clip: text;
        -webkit-text-fill-color: transparent;

    }
    &__text{
        @include text(text);
        color: white;
        width: 50.7rem;
    }
    &__form{
        position: relative;
        margin-top: 3.2rem;
    }
    &__input{
        box-shadow: 0px 4px 41px 0px #00000021;
        width: 66.1rem;
        border-radius: 14px;
        background: #FFFFFF1A;
        padding-top: 1.9rem;
        padding-left: 3.1rem;
        padding-bottom: 2.1rem;
        border: 1px solid;
        border-image-source: linear-gradient(180deg, rgba(255, 255, 255, 0.28) 0%, rgba(0, 0, 0, 0) 100%);
        @include text(body);
        color: white;
        display: block;

    }

    &__btn{
        width: 16.8rem;
        height: 4.9rem;
        background: #279D88;
        border-radius: 6.6rem;
        border: none;
        @include text(button);
        color: white;
        position: absolute;
        top: 0.8rem;
        right: 43rem;
        cursor: pointer;

    }
}



.start{
text-align: center;
display: flex;
align-items: center;
flex-direction: column;
padding-top: 12.8rem;


       

&__content{
    display: flex;
    justify-content: center;
    width: 100%;
    
}
&__title{
    @include text(h2);
    background: linear-gradient(91.92deg, #FFFFFF 29.24%, rgba(176, 250, 255, 0) 131.64%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    width: 54.3rem;

}
&__text{
    @include text(text);
    color: white;
    width: 54.3rem;
    
}
}
.bgword{
    position: relative;
    font-family: golos;
    top: -315px;
    left: 20px;
    font-size: 18rem;
    font-weight: 700;
    color: white;
    background: linear-gradient(91.92deg, rgba(255, 255, 255, 0.05) 29.24%, rgba(176, 250, 255, 0) 131.64%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    margin: 0;
    width: 64.9rem;
    
    
}

.step{
    display: flex;
    gap: 2.4rem;
    &__content{
        background: #151822;
        width: 36.5rem;
        height: 25.7rem;
        padding-left: 2.8rem;
        padding-top: 2.3rem;
        border-radius: .8rem;
        margin-bottom: 3.2rem;
    }
    &__text{
        color: white;
        width: 5rem;
        text-align: center;
        word-spacing: .3rem;
        @include text(body  );
        
        
    }
    &__line{
        border-top: 1px solid #FFFFFF1A;
        position: relative;
        height: 2rem;
        width: 30.3rem;
        top: 2.5rem;
        margin-left: 2rem;
    }
    &__title{
        color: white;
        @include text(h3)
    }
    &__imgO{
        float: right;
        position: relative;
        top: -52px;
    }
    &__imgTw{
        float: right;
        position: relative;
        top: -17px;
       
    }
    &__imgTr{
        float: right;
        position: relative;
        top: -40px;
    }
    
}


</style>