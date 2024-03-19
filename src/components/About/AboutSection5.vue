<template>
  <div class="alpha">

    <p class="section-header-1">What is Income Trade Asset <br/> Know more about us</p>
    <p class="section-header">An award winning Stock and Commodities Broker</p>

    <p class="text-1">Income Trade Asset is also known as Income Trade Asset: an award winning Stock and Commodities Broker,
      providing trading services and facilities to both retail and institutional clients. Through its policy of
      providing the best possible trading conditions to its clients and allowing both scalpers and traders using expert
      advisors unrestricted access to its liquidity, Income Trade Asset has positioned itself as the forex broker of
      choice for traders worldwide. At Income Trade Asset, we're dedicated to providing our clients with the most
      advanced and powerful trading tools in
      a wide range of markets For traders just starting out or seasoned traders already familiar with derivative
      trading, we offer the robust MetaTrader 4 and MetaTrader 5 platforms with the advantage of our competitive
      spreads and first class multi-lingual support. We also allow for flexible trading on a range of Forex and
      CFDs including Cryptocurrencies, Commodities, Indices and Binary Options through MetaTrader 4 and MetaTrader
      5.</p>

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
  /*padding-top: 4%;*/
  /*padding-bottom: 4%;*/
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
  background: #ffcf01;
  border: 1.5px solid #ffcf01;
  color: #ffffff;
}

.btn-2{
  background: #ffcf01;
  border: 1.5px solid #ffcf01;
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
  }
  .text-1{
    width: 95%;
    line-height: 1.6;
    font-size: 17px;
  }

}


@media (max-width: 500px) {

}
</style>