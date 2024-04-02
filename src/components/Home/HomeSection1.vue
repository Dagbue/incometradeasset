<template>
  <div class="alpha">

    <header>
      <h1>Discover the Benefits of Our Currency Trading Platform</h1>
    </header>
    <main class="grid-container">
      <article class="featured">
        <img src="https://assets.cmcmarkets.com/images/3_award_winning_platform_1_large.jpg" alt="featured img">
        <div>
          <h2>Experience the power of advanced technology in currency trading</h2>
          <p>Our platform utilizes cutting-edge technology to provide a seamless and efficient currency
            trading experience.</p>
          <div class="inner">

            <div class="inner-part-1">
              <h3 class="text-1">Secure Trading</h3>
              <p class="text-2">Trade with confidence knowing that your transactions are protected by state-of-the-art
                security measures.</p>
            </div>

            <div class="inner-part-1">
              <h3 class="text-1">User-Friendly</h3>
              <p class="text-2">Our intuitive interface makes currency trading accessible and easy for traders of all levels.</p>
            </div>

          </div>
        </div>
      </article>

      <article>
        <img src="https://images.ctfassets.net/fawq95y6n8yp/4h8q0OwWMZw5nqHSHolpMf/c8eccfac045bbe303efe8a94cc67bc1c/2687_tech_stocks.jpg?w=1100" alt="article img">
        <div>
          <h3>Trade with Confidence on Our Currency Trading Platform</h3>
          <p>Our currency trading platform offers a user-friendly interface and advanced trading tools.</p>
        </div>
      </article>
      <article>
        <img src="https://images.ctfassets.net/fawq95y6n8yp/3tFpoC0CTDeEs8oqg7RsvJ/518c2d725c87c6c854235a08b2896928/3037_gold_and_gbp.jpg?w=1100" alt="article img">
        <div>
          <h3>Access a Wide Range of Currency Pairs on Our Platform</h3>
          <p>With our currency trading platform, you can easily diversify your portfolio.</p>
        </div>
      </article>
      <article>
        <img src="https://images.ctfassets.net/fawq95y6n8yp/4HrL3h64pyCmO8AhxrHGoT/259f1301985cb54da63fb155c37b8833/2811_forex_trading_news.jpg?w=1100" alt="article img">
        <div>
          <h3>Stay Informed with Real-Time Market Data on Our Platform</h3>
          <p>Our currency trading platform provides up-to-date market analysis and insights.</p>
        </div>
      </article>
    </main>

  </div>
</template>

<script>
export default {
  name: "HomeSection1"
}
</script>

<style scoped>
ul, li {
  padding: 0;
  list-style-type: none;
}
h1,h2,h3 {
  color: #071333;
}
p {
  color: #0f171c;
}

header h1{
  font-size: 27px;
}

header {
  text-align: center;
  max-width: 1200px;
  margin: 50px auto;
  /*border-bottom: 1px solid #bbc7c7;*/
}
.grid-container {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 60px;
  max-width: 2200px;
  margin: 20px auto;
}
article.featured {
  grid-column: span 3;
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  padding-bottom: 40px;
}
article img, article.featured img {
  width: 100%;
  border: 4px solid #fff;
  border-radius: 8px;
}
article p, .article h3 {
  margin: 13px 0;
}

.inner{
  display: flex;
}

.inner-part-1{
  width: 50%;
}

/* responsive */
@media screen and (max-width: 980px) {
  article {
    grid-column: span 3;
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 90px;
    align-items: center;
  }
}

@media screen and (max-width: 760px) {
  article, article.featured {
    display: block;
    margin: 0 20px;
  }
  header h1{
    font-size: 25px;
    width: 95%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>