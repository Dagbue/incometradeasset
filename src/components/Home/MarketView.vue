<template>
  <div class="alpha">

    <div class="header">
      <p class="text-1">Optimize your product selection with minimal restrictions for a superior trading experience.</p>
      <p class="text-2">We transcend the typical brokerage experience. Our commitment lies in providing clients with outstanding
        trading conditions, a diverse range of CFD instruments, and highly competitive spreads tailored to meet the
        unique requirements of every trader.</p>
    </div>

    <div class="header-select">
      <p @click="changeScreen" class="btn">Cryptos</p>
      <p @click="changeScreen2" class="btn">Forex</p>
      <p @click="changeScreen3" class="btn">Stocks</p>
    </div>

    <crypto-table v-show="this.screen === 'crypto'"/>

    <forex-table v-show="this.screen === 'forex'"/>

    <stock-table v-show="this.screen === 'stocks'"/>

  </div>
</template>

<script>
import CryptoTable from "@/components/BaseComponents/tables/CryptoTable.vue";
import ForexTable from "@/components/BaseComponents/tables/ForexTable.vue";
import StockTable from "@/components/BaseComponents/tables/StockTable.vue";

export default {
  name: "MarketView",
  components: {StockTable, ForexTable, CryptoTable},
  data() {
    return {
      screen: "crypto",
    };
  },
  methods: {
    changeScreen() {
      this.screen = "crypto"
    },
    changeScreen2() {
      this.screen = "forex"
    },
    changeScreen3() {
      this.screen = "stocks"
    },
  }
}
</script>

<style scoped>
.alpha{
  margin-top: 5%;
  margin-bottom: 5%;
}
.header-select{
  display: flex;
  justify-content: center;
  gap: 20px;
  margin-bottom: 0;
  padding-bottom: 0;
}

.btn{
  background-color: #0f171c;
  border: 1px solid #0f171c;
  color: #ffffff;
  padding: 0.4em 30px 0.5em 30px;
  border-radius: 5px;
  position: relative;
  display: inline-block;
  margin: 0;
  text-decoration: none;
  -webkit-transition: all 0.1s ease;
  transition: all 0.25s ease;
}
.btn:hover{
  background-color: #ccaa16;
  border: 1px solid #ccaa16;
  color: #FFFFFF;
}

.text-1{
  font-size: 26px;
  text-align: center;
  color: #071333;
  padding-bottom: 15px;
  width: 50%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.text-2{
  font-size: 16px;
  text-align: center;
  color: #0f171c;
  padding-bottom: 2%;
  width: 60%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}


@media (max-width: 990px) {

}

@media (max-width: 700px){

  .header{
    width: 95%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }

  .text-1{
    font-size: 24px;
    padding-bottom: 20px;
  }

  .text-2{
    font-size: 16px;
  }

  .header-select{
    gap: 5px;
    margin-top: 3%;
  }

}

@media (max-width: 500px){

}

</style>