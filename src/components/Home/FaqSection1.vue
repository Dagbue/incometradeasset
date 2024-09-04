<template>
  <div class="alpha">


    <div class="section-1">

      <p class="header">General FAQs</p>

      <section>
        <details>
          <summary>
            WHAT IS COIN MATRIX INVESTMENT
          </summary>
          <p>
            Coin Matrix Investment is an officially registered company and conducts
            business under the laws of the UK Government. The company is involved
            in Stocks, options CFD , Forex and crypto. Also trading other valuable
            commodities/assets which we offer to our clients to earn from using a
            single trading account.
          </p>
        </details>
        <details>
          <summary>
            HOW SAFE ARE MY INVESTMENTS IN YOUR COMPANY
          </summary>
          <p>
            It is absolutely safe because all our technical experts are extremely
            experienced professionals; our Stocks, options CFD , Forex and crypto sourcing and
            other investment strategies are proven to work.
          </p>
        </details>

        <details>
          <summary>
            HOW CAN I MAKE SURE YOUR COMPANY IS A REAL AND NOT A FAKE ONE
          </summary>
          <p>
            Coin Matrix Investment is officially incorporated with the USA
            Companies Office. verify registration: (click here)
<!--            <a href="https://find-and-update.company-information.service.gov.uk/company/11557864">-->
<!--              https://find-and-update.company-information.service.gov.uk/company/11557864-->
<!--            </a>-->
          </p>
        </details>
        <details>
          <summary>
            CAN I LOOSE MONEY IF I INVEST NOW?
          </summary>
          <p>
            In accordance to investment laws of the FCA with over £3Billion
            investment security, we never worry about those rainy days in global
            trades and projects as we have our investors covered
          </p>
        </details>

        <details>
          <summary>
            DO YOU PROVIDE PROOF OF YOUR TRADING  ACTIVITIES
          </summary>
          <p>
            No, at the moment this is a closed information, but in the future we
            plan to publish our trade reports regularly. We will announce further,
            follow our news.
          </p>
        </details>


      </section>

    </div>

    <br/>
    <br/>



  </div>
</template>

<script>
export default {
  name: "FaqSection1"
}
</script>

<style scoped>
.section-1{
  padding-top: 4%;
  display: flex;
  justify-content: space-evenly;
  /*align-content: center;*/
  /*align-items: center;*/
}
.header{
  font-stretch: normal;
  font-style: normal;
  font-weight: 900;
  letter-spacing: normal;
  font-size: 23px;
  line-height: 1.26;
  margin: 0;
  color: #0f171c;
  width: 25%;
}
.lawrence{
  padding-left: 5%;
}
.lawrence li{
  padding-bottom: 2px;
}
section {
  width: 42%;
  /*margin: auto;*/
}

details[open] summary ~ * {
  animation: open 0.4s ease-in;
}

@keyframes open {
  0% {
    transform: translateY(-60px);
    opacity: 0;
  }
  50% {
    transform: translateY(0);
    opacity: 1;
  }
  60% {
    transform: translateX(10px);
  }
  70% {
    transform: translateX(-10px);
  }
  80% {
    transform: translateX(5px);
  }
  90% {
    transform: translateX(-5px);
  }
  100% {
    transform: translateX(0);
    opacity: 1;
  }
}
details summary::-webkit-details-marker {
  display: none;
}

details summary {
  width: 100%;
  position: relative;
  cursor: pointer;
  font-size: 0.9rem;
  font-weight: 900;
  list-style: none;
  /*padding-top: 18px;*/
  /*padding-bottom: 10px;*/
  text-transform: uppercase;
  color: #222222;
}

details summary:after {
  content: "+";
  color: #0f171c;
  position: absolute;
  font-size: 1.7rem;
  line-height: 0;
  margin-top: 0.75rem;
  right: 0;
  font-weight: bold;
  transform-origin: center;
  transition: 200ms linear;
}
details[open] summary:after {
  transform: rotate(45deg);
  font-size: 2rem;
}
details summary {
  outline: 0;
}
details p {
  font-size: 16px;
  margin: 0 0 1rem;
  padding-top: 1rem;
}
details {
  /*box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);*/
  position: relative;
  padding: 15px;
  margin-bottom: 2%;
  /*border-radius: 5px;*/
  border-bottom: solid 0.125rem #e7eaf0;
}



@media (max-width: 700px){
  .section-1{
    display: block;
    width: 100%;
  }
  .header{
    width: 100%;
    text-align: center;
  }
  .details summary {
    font-size: 20px;
  }
  details p {
    font-size: 16px;
    margin: 0 0 1rem;
    padding-top: 1rem;
  }
  summary{
    font-size: 20px;
  }
  section {
    width: 82%;
    display: block;
    margin-left: auto;
    margin-right: auto;
  }
}
</style>