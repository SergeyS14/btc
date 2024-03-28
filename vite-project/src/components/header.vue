
<script>
import IconBase from './common/IconBase.vue';
import IconLogo from './common/IconLogo.vue';
import IconLng from './common/IconLng.vue';

import axios from 'axios';

export default {
  components:{IconLng, IconLogo,IconBase},
  data() {
    return {
      info: null,
      loading: true,
      errored: false
    };
  },
  filters: {
    currencydecimal(value) {
      return value.toFixed(2);
    }
  },
  mounted() {
    axios
      .get('https://api.coindesk.com/v1/bpi/currentprice.json')
      .then(response => {
        this.info = response.data.bpi;
      })
      .catch(error => {
        console.log(error);
        this.errored = true;
      })
      .finally(() => (this.loading = false));
  }
  
};

</script>

<template>
    <header class="header " >
      <icon-base width="42" height="42" class="header__logo" icon-name="Logo"><icon-logo /></icon-base>
  <nav  class="header__nav">
      <ul class="header__list">
          <li class="header__list__item"><a>Функции</a></li>
          <li class="header__list__item"><a>Кошельки</a></li>
          <li class="header__list__item"><a>Участие</a></li>
          <li class="header__list__item"><a>Ресурсы</a></li>
          <li class="header__list__item"><a>Новости</a></li>
          <li class="header__list__item"><a>O BTCA</a></li>
      </ul>
  </nav>
  <div class="header__btn">
    <button  class="header__btn__item">
      <icon-base class="header__lng" icon-name="Lng"><icon-lng /></icon-base>
      RUS
    </button>
  </div>
  <div class="header__btc">
  <p>Курс BTC:</p>

  <section v-if="errored">
    <p>К сожалению, в данный момент мы не можем получить эту информацию, повторите попытку позже.</p>
  </section>

  <section class="header__btc__loading" v-else>
    <div v-if="loading">Loading...</div>

    <div
      v-else
      v-for="currency in info"
      class="header__btc__item"
    >
      <span >
        <span  v-html="currency.symbol"></span>{{ currency.rate_float | currencydecimal }}
    </span>
    </div>
  </section>
</div>

</header>
</template>

<style lang="scss" scoped>

@import '../styles/variables.scss';
.header{
  display: flex;
  justify-content: space-around;
  align-items: center;
  height: 6.8rem;
  width: 100%;
  margin: 0;
  background: linear-gradient(267.43deg, rgba(0, 255, 163, 0.12) 36.58%, rgba(31, 26, 255, 0.2) 80.91%);
  box-shadow: 0px 4px 40px 0px #0000000D;


  &__logo{
    width: 4.2rem;
    height: 4.2rem;
  }

  &__nav{
    display: flex;
    
  }

  &__list{
    display: flex;
    gap: 4.3rem;
    list-style-type: none;
    cursor: pointer;
    color: #FFFFFF6B;
    @include text(menu)
  }

  &__list__item:hover{
    color:#FFFFFF ;
  }

  &__btn{

    &__item{
      width: 7.6rem;
      height: 3.3rem;
      display: flex;
      align-items: center;
      gap: 0.5rem;
      color: rgb(255, 255, 255);
      font-size: 1.4rem;
      border: 0.5px solid;
      border-image-source: linear-gradient(180deg, rgba(255, 255, 255, 0.7) 0%, rgba(225, 225, 225, 0.252) 100%);
      box-shadow: 0px 4px 9px 0px #B0B0B01A;
      cursor: pointer;
      border-radius: 0.8rem;
      background: #FFFFFF26;
      

    }
 }

 .header__btc{
  display: flex;
  align-items: center;
  font-size: 1.4rem;
  gap: 1.1rem;
  color: white;
 

 }
}

.header__lng{
  width: 2.2rem;
  height: 2.2rem;
}

</style>
