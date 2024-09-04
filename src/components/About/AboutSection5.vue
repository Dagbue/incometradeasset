<template>
  <div class="alpha">

    <p class="section-header-1">What is Coin Matrix Investment Know more about us</p>
    <p class="section-header">An award winning Stock and Commodities Broker</p>

    <p class="text-1">Coin Matrix Investment is an award-winning broker for stocks and commodities, catering to both
      retail and institutional clients. It offers optimal trading conditions, supporting scalpers and users of
      expert advisors without limiting access to liquidity. This has made it a preferred broker globally. Coin Matrix
      Investment emphasizes on equipping its clients with advanced trading tools across various markets. It provides
      the MetaTrader 4 and MetaTrader 5 platforms, accommodating both new and experienced derivative traders with
      competitive spreads and exceptional multi-lingual support. Additionally, it enables flexible trading in Forex,
      CFDs, Cryptocurrencies, Commodities, Indices, and Binary Options through these platforms.</p>

    <div class="btn-part">
      <p class="btn-1">Register</p>
      <p class="btn-2">Log In</p>
    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection5"
}
</script>

<style scoped>
/*.alpha{*/
/*  background-color: #f4f5f6;*/
/*  padding-bottom: 4%;*/
/*  padding-top: 4%;*/
/*}*/
.alpha{
  /*border-bottom: 1px solid #c9c9c9;*/
  background-image: url("https://d33vw3iu5hs0zi.cloudfront.net/media/xxxl_exness_deposits_withdrawals_926ba82c4b.jpg");
  background-color: #cccccc;
  background-position: center;
  background-repeat: no-repeat;
  background-size: cover;
  position: relative;
  padding-top: 5%;
  padding-bottom: 5%;
  margin-top: 5%;
  /*margin-bottom: 5%;*/
}
.section-header{
  font-size: 17px;
  color: #ffffff;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
}
.section-header-1{
  font-size: 30px;
  color: #ffffff;
  font-weight: bold;
  text-align: center;
  padding-bottom: 1%;
}
.text-1{
  width: 75%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
  line-height: 1.7;
  margin-top: 2%;
  color: #ffffff;
  font-size: 18px;
}
.btn-part{
  display: flex;
  align-items: center;
  align-content: center;
  justify-content: center;
  padding-top: 3%;
}

.btn-1{
  background: #0f171c;
  border: 1.5px solid #0f171c;
  padding: 10px 25px;
  margin-right: 3%;
  color: #ffffff;
  width: 200px;
  text-align: center;
  border-radius: 4px;
}

.btn-1:hover{
  background: #ccaa16;
  border: 1.5px solid #ccaa16;
  color: #ffffff;
}

.btn-2{
  background: #ccaa16;
  border: 1.5px solid #ccaa16;
  color: #ffffff;
  padding: 10px 25px;
  margin-right: 3%;
  width: 200px;
  text-align: center;
  border-radius: 4px;
}

.btn-2:hover{
  background: #0f171c;
  border: 1.5px solid #0f171c;
  color: #ffffff;
}


@media (max-width: 700px) {
  .section-header-1{
    font-size: 25px;
    width: 95%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
  .text-1{
    width: 95%;
    line-height: 1.6;
    font-size: 17px;
  }

  .section-header{
    font-size: 17px;
    margin-left: 5%;
    margin-right: 5%;
  }

  .alpha{
    padding-top: 10%;
    padding-bottom: 10%;
  }

  .btn-1{
    width: 160px;
  }

  .btn-2{
    width: 160px;
  }

}


@media (max-width: 500px) {

}
</style>