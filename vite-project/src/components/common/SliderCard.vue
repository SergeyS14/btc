<template>
    <div :class="['SlideCard',$style.SlideCard,{[$style['_active']]:active}]" :style="{backgroundImage:`url(${card.img})`}">
        <span :class="$style.subtitle">{{ card.subtitle }}</span>
        <span :class="$style.title">{{ card.title }}</span>
        <span :class="$style.text">{{ card.text }}</span>
        <button :class="$style.btn">Перейти и получить</button>
    </div>

</template>
<script>
export default{
    name:'SliderCard',
    props:{
        card:{
            type: Object,
            required:true,
        },
        active:{
            type: Boolean,
            default: false,
            required: false
        }
    }
}
</script>
<style lang="scss" module>

.SlideCard{
    display: flex;
    flex-direction: column;
    width: calc(33% - 25px);
    height: 46rem;
    background-color: rgba(21, 24, 34, 1);
    opacity: .5;
    transition: all .3s ease-in-out;
    cursor: pointer;
    padding: 3rem;
    border-radius: 0.8rem;
    background-repeat: no-repeat;
    background-position: bottom right;
    &:global(.swiper-slide){
        transform: translateY(100px);
    }
    
    
}
.SlideCard._active{
    opacity: 1;
    transform: translateY(0);
}

.subtitle{
    @include text(text);
    color: white;
    
}
.title{
    color: white;
    @include text(h3)
    
}
.text{
    color: white;
    margin-top: 2rem;
    margin-bottom: 2rem;
    @include text(body)
    
}

.btn{
        width: 22.4rem;
        height: 5.4rem;
        color: rgb(255, 255, 255);
        background: $green;
        border-radius: 1.2rem;
        box-shadow: 0px 8px 16px 0px rgba(75, 72, 241, 0.19);
        @include text(button)

    }

</style>