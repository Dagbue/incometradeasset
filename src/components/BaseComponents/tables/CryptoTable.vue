<template>

    <div class="tables">

      <div class="tradingview-widget-container">
        <div class="tradingview-widget-container__widget"></div>
      </div>

    </div>

</template>

<script>
export default {
  name: "CryptoTable",
  mounted() {
    const script = document.createElement("script");
    script.type = "text/javascript";
    script.src = "https://s3.tradingview.com/external-embedding/embed-widget-screener.js";
    script.async = true;

    script.innerHTML = JSON.stringify({
      "width": "100%",
      "height": "600",
      "defaultColumn": "overview",
      "screener_type": "crypto_mkt",
      "displayCurrency": "USD",
      "colorTheme": "light",
      "locale": "en",
      "isTransparent": false
    });

    this.$el.querySelector(".tradingview-widget-container__widget").appendChild(script);

  }
}
</script>

<style scoped>
.tables{
  margin-left: 5%;
  margin-right: 5%;
  margin-top: 1%;
}
</style>