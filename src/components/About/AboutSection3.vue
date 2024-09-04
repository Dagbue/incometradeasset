<template>
  <div class="alpha">
    <p class="section-header-1">There’s a time and a place for risk</p>
    <p class="section-header">Your funds and data are always secure. With Coin Matrix Investment you’re protected
      by industry-leading protocols.</p>


    <div class="section-alpha">

      <div class="section-1">

        <div class="text-part">
          <p class="text-1">Transparent trading practices</p>
          <p class="text-2">Backtest your trading strategy with our full tick history. See for yourself how reliable
            our pricing and execution are.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Multiple regulatory licenses</p>
          <p class="text-2">We are licensed and regulated by leading international governing bodies. Trade knowing
            your financial data is protected.</p>
        </div>

        <div class="text-part">
          <p class="text-1">Segregated accounts</p>
          <p class="text-2">Your funds are always kept separate from company funds, so you’ll always have access to
            them. No ifs, no buts.</p>
        </div>


      </div>

      <div class="section-2">

        <img src="https://d33vw3iu5hs0zi.cloudfront.net/media/xl_exness_why_exness1_1b2dac8fa4.png" alt="image" class="image" />

      </div>

    </div>

  </div>
</template>

<script>
export default {
  name: "AboutSection3"
}
</script>

<style scoped>
.alpha{
  /*background-color: #f0f2f4;*/
  padding-bottom: 3%;
  padding-top: 3%;
}

.section-1{
  width: 50%;
}

.section-2{
  width: 50%;
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
.section-alpha{
  display: flex;
  justify-content: space-around;
  align-items: center;
  align-content: center;
  margin-top: 3%;
}

.image{
  width: 75%;
  display: block;
  margin-right: auto;
  margin-left: auto;
}

.text-part{
  width: 75%;
  display: block;
  margin-right: auto;
  margin-left: auto;
  margin-bottom: 5%;
}

.text-1{
  font-size: 28px;
  line-height: 26px;
  font-weight: 500;
  white-space: pre-line;
  margin-bottom: 15px;
}

.text-2{
  margin: 0;
  font-size: 17px;
  white-space: pre-line;
  line-height: 1.4;
}

@media (max-width: 700px) {
  .section-header{
    font-size: 16px;
    margin-left: 8%;
    margin-right: 8%;
  }
  .section-header-1{
    font-size: 28px;
  }
  .section-alpha{
    display: block;
  }
  .section-1{
    width: 100%;
  }

  .section-2{
    width: 100%;
  }

  .text-1{
    font-size: 26px;
    line-height: 24px;
    margin-bottom: 13px;
  }

  .text-2{
    font-size: 16px;
    line-height: 1.3;
  }
  .image{
    width: 90%;
  }
}


@media (max-width: 500px) {

}
</style>