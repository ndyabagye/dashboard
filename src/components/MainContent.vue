<template>
  <div class="content">
    <Search />
    <div class="cards px-5 mt-5 gap-3">
      <Card  v-for="card in cardData" :key="card.id" :color="card.color" :title="card.title" :btc="card.btc" :usd="card.usd" :svg="card.svg" />
    </div>
  </div>
</template>

<script>
import Search from '@/components/Search.vue';
import Card from '@/components/Card.vue';
import Bitcoin from '@/svg/bitcoin.svg';
import Ethereum from '@/svg/ethereum.svg';
import Litecoin from '@/svg/litecoin.svg';


export default {
  components: {
    Search,
    Card,
  },
  data() {
    return {
      cardData: [
        {
          id: 1,
          title: 'Bitcoin',
          btc: '0.2231345 BTC',
          usd: '11,032.24 USD',
          color:"#fdedd5",
          svg: Bitcoin,

        },
         {
          id: 2,
          title: 'Ethereum',
          btc: '10.612356 BTC',
          usd: '1242.31 USD',
          color:"#fde5f9",
          svg: Ethereum
        },
         {
          id: 3,
          title: 'Litecoin',
          btc: '120.235 BTC',
          usd: '37,747.78 USD',
          color:"#b7e0e9",
          svg: Litecoin
        },
      ],
    };
  },
};
</script>

<style>
.content {
  background-color: #ffffff;
}
.cards {
  display: grid !important;
  grid-template-columns: 1fr 1fr 1fr !important;
}
</style>
