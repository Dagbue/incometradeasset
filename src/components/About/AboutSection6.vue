<template>
  <div class="section-alpha">

    <p class="section-header-1">Why Coin Matrix Investment</p>
    <p class="section-header">We believe in fair trading and offer better-than-market conditions for all.</p>
    <div class="section-content">

      <div class="section-content-1" >
        <div class="box">
          <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/instant_withdrawals_96c97dca73.svg" class="about-image" alt="assets-image"/>
          <h3>Instant withdrawals</h3>
          <p>Remain in control of your funds. Simply choose your preferred payment method, make a withdrawal
            request, and enjoy instant automatic approval.</p>
        </div>
        <div class="box">
          <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/exness_fast_execution_57c7f263d9.svg" class="about-image" alt="assets-image"/>
          <h3>Ultra-fast execution</h3>
          <p>Stay ahead of trends with lightning-fast execution. Get your orders executed in milliseconds on all
            available platforms at Income Trade Asset.</p>
        </div>
        <div class="box">
          <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/exness_stop_out_protection_3058b9de65.svg" class="about-image" alt="assets-image"/>
          <h3>Stop Out Protection</h3>
          <p>Enjoy our unique Stop Out Protection feature. Delay and sometimes completely avoid stop outs while
            trading with Coin Matrix Investment.</p>
        </div>
      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection6"
}
</script>

<style scoped>

.section-alpha{
  /*background-color: #f0f2f4;*/
  padding-bottom: 5%;
  padding-top: 5%;
}

.section-header{
  font-size: 17px;
  color: #0f171c;
  text-align: center;
  font-weight: 300;
  margin-left: 23%;
  margin-right: 23%;
}
.section-header-1{
  font-size: 30px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  padding-bottom: 1%;
}

.box{
  background-color: #ffffff;
  box-shadow:  20px 20px 60px #d9d9d9,
  -20px -20px 60px #ffffff;
  padding: 15px;
  border-radius: 5px;
  margin-bottom: 12px;
  margin-top: 4%;
  width: 330px;
  height: 300px;
}


.section-content-1{
  display: flex;
  justify-content: space-evenly;
}

.about-image{
  display: block;
  margin-left: auto;
  margin-right: auto;
  height: 60px;
  width: 60px;
  object-fit: cover;
  margin-top: 7%;
}
.about-image-1{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 30%;
}
.about-image-2{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 37%;
}
.about-image-3{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 29%;
}

.box h3{
  padding-top: 20px;
  color: #222222;
  font-weight: bold;
  text-align: center;
  margin-bottom: 10px;
}

.box p{
  color: #222222;
  text-align: center;
  font-size: 15px;
  line-height: 1.5;
}

@media (max-width: 700px) {
  .section-header{
    font-size: 15px;
    margin-left: 10%;
    margin-right: 10%;
  }
  .section-content-1{
    display: flex;
    flex-direction: column-reverse;
    justify-content: space-evenly;
  }

  .section-header-1{
    font-size: 26px;
  }

  .box{
    /*margin-left: 10%;*/
    /*margin-right: 10%;*/
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}


@media (max-width: 500px) {
}
</style>