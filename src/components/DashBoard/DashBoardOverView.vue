<template>
  <div class="alpha">
    <div class="section-2">

      <div class="section-2-part-1">
        <div class="lawrence bottom">
          <p  @click="toggleScreen" class="trade-btn-1">Trade Forex</p>
          <p @click="toggleScreen2" class="trade-btn-2">Trade Crypto }</p>
        </div>
        <div class="lawrence">
          <p @click="toggleScreen3" class="trade-btn-3">Trade CFD</p>
          <p @click="toggleScreen4" class="trade-btn-4">Trade Stocks</p>
        </div>
      </div>

      <div class="section-2-part-2">

        <p class="fund-wallet" @click="onPostClick">
          <i class='bx bx-plus' ></i>
          Fund Wallet
        </p>

      </div>
    </div>

    <iframe scrolling="no" allowtransparency="true" frameborder="0" src="https://www.tradingview-widget.com/embed-widget/ticker-tape/#%7B%22colorTheme%22%3A%22dark%22%2C%22width%22%3A%22100%25%22%2C%22height%22%3A46%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22ticker-tape%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeCrypto%22%7D" title="ticker tape TradingView widget" lang="en" style="user-select: none; box-sizing: border-box; display: block; height: 65px; width: 99%; margin-bottom: 1%;"></iframe>

    <p v-show="this.UserDetails.user.userStatus === 'unVerified'" class="text-2">Your Account is not verified.</p>

<!--    <div style="color: white;" id="app">-->
<!--      <h1>Dollar to Bitcoin Converter</h1>-->
<!--      <input type="number" v-model="dollars" placeholder="Enter amount in dollars" />-->
<!--      <button @click="convertToBitcoin">Convert</button>-->
<!--      <p style="color:#ffffff;" v-if="bitcoin">Equivalent in Bitcoin: {{ bitcoin }}</p>-->
<!--    </div>-->

    <div class="law">
      <div class="section-3">

        <div class="section-3-content">
          <div class="content-1">
            <p class="content-1-text-1">BTC Balance</p>
            <div>
<!--              <p class="content-1-text-2" v-if="approved === 'approved'">£ {{this.contacts.deposit}}</p>-->
<!--              <p class="content-1-text-2" v-else-if="approved === 'Pending'">£ ...</p>-->
              <p class="content-1-text-2" >{{bitcoin}}</p>
            </div>
          </div>
          <div class="content-2">
            <img src="@/assets/wallet-number-icon.svg" alt="wallet-balance-icon"/>
          </div>
        </div>

        <div class="vl-2"></div>

        <div class="section-3-content">
          <div class="content-1">
            <p class="content-1-text-1">Main Balance</p>
            <div>
<!--              <p class="content-1-text-2" v-if="approved2 === 'approved'">£ {{this.contacts.withdrawal}}</p>-->
<!--              <p class="content-1-text-2" v-else-if="approved2 === 'Pending'">£ ...</p>-->
              <p class="content-1-text-2" >$ {{UserDetails.user.totalDepositedAmount + UserDetails.user.totalWithdrawals | formatAmount2}}</p>
            </div>
          </div>
          <div class="content-2">
            <img src="@/assets/wallet-number-icon.svg" alt="wallet-balance-icon"/>
          </div>
        </div>

        <div class="vl-2"></div>

        <div class="section-3-content">
          <div class="content-1">
            <p class="content-1-text-1">Invested Amount</p>
            <div>
<!--              <p class="content-1-text-2" v-if="approved === 'approved'">£ {{this.contacts.profits}}</p>-->
<!--              <p class="content-1-text-2" v-else-if="approved === 'Pending'">£ ...</p>-->
              <p class="content-1-text-2" >$ {{UserDetails.user.totalDepositedAmount | formatAmount2}}</p>
            </div>
          </div>
          <div class="content-2">
            <img src="@/assets/wallet-number-icon.svg" alt="wallet-balance-icon"/>
          </div>
        </div>

        <div class="vl-2"></div>

        <div class="section-3-content">
          <div class="content-1">
            <p class="content-1-text-1">Currency</p>
            <div>
<!--              <p class="content-1-text-2" v-if="approved === 'approved'">£ {{this.contacts.bonusMain}}</p>-->
<!--              <p class="content-1-text-2" v-else-if="approved === 'Pending'">£ ...</p>-->
              <p class="content-1-text-2" >Dollars</p>
            </div>
          </div>
          <div class="content-2">
            <img src="@/assets/wallet-number-icon.svg" alt="wallet-balance-icon"/>
          </div>
        </div>

      </div>
    </div>

    <div v-show="this.screen1 === 'Forex'"  class="separate">
      <div class="tradingview_7a2ab-wrapper"
           style="position: relative;
               box-sizing: content-box;
               width: 98%;
               display: block;
               margin-left: auto;
               margin-right: auto;
               height: 560px;"
      >
          <iframe title="advanced chart TradingView widget" lang="en" id="tradingview_7a2ab" frameborder="0"
                  allowtransparency="true" scrolling="no" allowfullscreen="true"
                  src="https://s.tradingview.com/widgetembed/?hideideas=1&amp;overrides=%7B%7D&amp;enabled_features=%5B%5D&amp;disabled_features=%5B%5D&amp;locale=en#%7B%22symbol%22%3A%22OANDA%3AUSDCAD%22%2C%22frameElementId%22%3A%22tradingview_7a2ab%22%2C%22interval%22%3A%22D%22%2C%22hide_side_toolbar%22%3A%220%22%2C%22allow_symbol_change%22%3A%221%22%2C%22save_image%22%3A%221%22%2C%22studies%22%3A%22%5B%5D%22%2C%22theme%22%3A%22dark%22%2C%22style%22%3A%221%22%2C%22timezone%22%3A%22Etc%2FUTC%22%2C%22withdateranges%22%3A%221%22%2C%22show_popup_button%22%3A%221%22%2C%22studies_overrides%22%3A%22%7B%7D%22%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22chart%22%2C%22utm_term%22%3A%22OANDA%3AUSDCAD%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2F%22%7D"
                  style="width: 100%; height: 100%; margin: 0px !important; padding: 0px !important;"></iframe>
        </div>
      <form ref="myForm" class="form-part" @submit.prevent="placeTrade">

        <div class="form-header">
          <p style="font-weight: bold;color: #FFFFFF;">TRADE FOREX - PLACE TRADE</p>
        </div>

        <div class="form-group">
          <label class="label">Amount</label>
          <input type="number" placeholder="Enter Amount"  name="Amount" v-model="amountTrade" required/>
        </div>

        <div class="form-group">
          <label class="label">Trading Pair</label>
          <select name="tradingPair" id="tradingPair" required v-model="symbolTraded" >
            <option selected disabled value="">Choose Trading Pair</option>
            <option :value="null" disabled>Choose Trading Pair</option>
            <option value="USD/CAD">USD/CAD</option>
            <option value="USD/CHF">USD/CHF</option>
            <option value="USD/JPY">USD/JPY</option>
            <option value="EUR/USD">EUR/USD</option>
            <option value="GBP/USD">GBP/USD</option>
            <option value="NZD/USD">NZD/USD</option>
            <option value="AUD/CAD">AUD/CAD</option>
            <option value="AUD/USD">AUD/USD</option>
            <option value="EUR/GBP">EUR/GBP</option>
            <option value="GBP/AUD">GBP/AUD</option>
            <option value="EUR/AUD">EUR/AUD</option>
            <option value="AUD/CHF">AUD/CHF</option>
            <option value="GBP/CHF">GBP/CHF</option>
            <option value="GBP/JPY">GBP/JPY</option>
            <option value="AUD/JPY">AUD/JPY</option>
            <option value="EUR/JPY">EUR/JPY</option>
            <option value="AUD/NZD">AUD/NZD</option>
            <option value="EUR/CHF">EUR/CHF</option>
            <option value="NZD/JPY">NZD/JPY</option>
            <option value="CAD/CHF">CAD/CHF</option>
            <option value="GBP/NZD">GBP/NZD</option>
            <option value="CHF/JPY">CHF/JPY</option>
            <option value="NZD/CAD">NZD/CAD</option>
            <option value="NZD/CHF">NZD/CHF</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Interval (Time)</label>
          <select name="tradeInterval" id="tradeInterval" required v-model="tradeTime" >
            <option selected disabled value="">Trade Interval (Time)</option>
            <option :value="null" disabled>Trade Interval (Time)</option>
            <option value="1 min">1 min</option>
            <option value="3 min">3 min</option>
            <option value="5 min">5 min</option>
            <option value="15 mins">15 mins</option>
            <option value="30 mins">30 mins</option>
            <option value="1 hr">1 hr</option>
            <option value="2 hr">2 hr</option>
            <option value="1 day">1 day</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Type</label>
          <select name="tradeType" id="tradeType" required v-model="tradeType">
            <option selected disabled value="">Trade Type</option>
            <option :value="null" disabled>Trade Type</option>
            <option value="Buy">Buy</option>
            <option value="Sell">Sell</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Leverage</label>
          <select name="tradeLeverage" id="tradeLeverage" required v-model="leverage" >
            <option selected disabled value="">Trade Leverage</option>
            <option :value="null" disabled>Trade Leverage</option>
            <option value="0.5X">0.5X</option>
            <option value="1.0X">1.0X</option>
            <option value="1.5X">1.5X</option>
            <option value="2.0X">2.0X</option>
            <option value="5X">5X</option>
            <option value="10X">10X</option>
          </select>
        </div>

        <base-button  style="  background-color: #5d78ff;border: 1px solid #5d78ff;" :loading="loading" >Place Trade </base-button>
      </form>
    </div>

    <div v-show="this.screen1 === 'Crypto'"  class="separate">


          <div id="tradingview_1a10b-wrapper"
               style="position: relative;
               box-sizing: content-box;
               width: 98%;
               display: block;
               margin-left: auto;
               margin-right: auto;
               height: 560px;"
          >
            <iframe title="advanced chart TradingView widget" lang="en" id="tradingview_1a10b" frameborder="0"
                    allowtransparency="true" scrolling="no" allowfullscreen="true"
                    src="https://s.tradingview.com/widgetembed/?hideideas=1&amp;overrides=%7B%7D&amp;enabled_features=%5B%5D&amp;disabled_features=%5B%5D&amp;locale=en#%7B%22symbol%22%3A%22BITSTAMP%3ABTCUSD%22%2C%22frameElementId%22%3A%22tradingview_1a10b%22%2C%22interval%22%3A%22D%22%2C%22hide_side_toolbar%22%3A%220%22%2C%22allow_symbol_change%22%3A%221%22%2C%22save_image%22%3A%221%22%2C%22details%22%3A%221%22%2C%22studies%22%3A%22%5B%5D%22%2C%22theme%22%3A%22dark%22%2C%22style%22%3A%221%22%2C%22timezone%22%3A%22Etc%2FUTC%22%2C%22studies_overrides%22%3A%22%7B%7D%22%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22chart%22%2C%22utm_term%22%3A%22BITSTAMP%3ABTCUSD%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeCrypto%22%7D" style="width: 100%; height: 100%; margin: 0px !important; padding: 0px !important;"></iframe>
          </div>


      <form ref="myForm" class="form-part" @submit.prevent="placeTrade">

        <div class="form-header">
          <p style="font-weight: bold;color: #FFFFFF;">TRADE CRYPTO - PLACE TRADE</p>
        </div>

        <div class="form-group">
          <label class="label">Amount</label>
          <input type="number" placeholder="Enter Amount"  name="Amount" v-model="amountTrade"  required/>
        </div>

        <div class="form-group">
          <label class="label">Trading Pair</label>
          <select name="tradingPair" id="tradingPair" required v-model="symbolTraded" >
            <option selected disabled value="">Choose Trading Pair</option>
            <option :value="null" disabled>Choose Trading Pair</option>
            <option value="BCH/BTC">BCH/BTC</option>
            <option value="BCH/EUR">BCH/EUR</option>
            <option value="BCH/GBP">BCH/GBP</option>
            <option value="BTC-EOS">BTC-EOS</option>
            <option value="BTC/EUR">BTC/EUR</option>
            <option value="BTC/GBP">BTC/GBP</option>
            <option value="BTC/USD">BTC/USD</option>
            <option value="BTC/USDC">BTC/USDC</option>
            <option value="EOS/BTC">EOS/BTC</option>
            <option value="EOS/EUR">EOS/EUR</option>
            <option value="EOS/USD">EOS/USD</option>
            <option value="ETC/BTC">ETC/BTC</option>
            <option value="ETC/EUR">ETC/EUR</option>
            <option value="ETC/GBP">ETC/GBP</option>
            <option value="ETC/USD">ETC/USD</option>
            <option value="ETH/BTC">ETH/BTC</option>
            <option value="ETH/EUR">ETH/EUR</option>
            <option value="ETH/GBP">ETH/GBP</option>
            <option value="ETH/USD">ETH/USD</option>
            <option value="LTC/BTC">LTC/BTC</option>
            <option value="LTC/EUR">LTC/EUR</option>
            <option value="LTC/GBP">LTC/GBP</option>
            <option value="LTC/USD">LTC/USD</option>
            <option value="MKR/BTC">MKR/BTC</option>
            <option value="PCP-BTC">PCP-BTC</option>
            <option value="REP/BTC">REP/BTC</option>
            <option value="REP/USD">REP/USD</option>
            <option value="TXR/GBP">TXR/GBP</option>
            <option value="XLM/BTC">XLM/BTC</option>
            <option value="XLM/EUR">XLM/EUR</option>
            <option value="XLM/USD">XLM/USD</option>
            <option value="XRP/BTC">XRP/BTC</option>
            <option value="XRP/EUR">XRP/EUR</option>
            <option value="XRP/USD">XRP/USD</option>
            <option value="ZEC/BTC">ZEC/BTC</option>
            <option value="ZRX/BTC">ZRX/BTC</option>
            <option value="ZRX/EUR">ZRX/EUR</option>
            <option value="ZRX/USD">ZRX/USD</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Interval (Time)</label>
          <select name="tradeInterval" id="tradeInterval" required v-model="tradeTime" >
            <option selected disabled value="">Trade Interval (Time)</option>
            <option :value="null" disabled>Trade Interval (Time)</option>
            <option value="1 min">1 min</option>
            <option value="3 min">3 min</option>
            <option value="5 min">5 min</option>
            <option value="15 mins">15 mins</option>
            <option value="30 mins">30 mins</option>
            <option value="1 hr">1 hr</option>
            <option value="2 hr">2 hr</option>
            <option value="1 day">1 day</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Type</label>
          <select name="tradeType" id="tradeType" required v-model="tradeType" >
            <option selected disabled value="">Trade Type</option>
            <option :value="null" disabled>Trade Type</option>
            <option value="Buy">Buy</option>
            <option value="Sell">Sell</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Leverage</label>
          <select name="tradeLeverage" id="tradeLeverage" required v-model="leverage" >
            <option selected disabled value="">Trade Leverage</option>
            <option :value="null" disabled>Trade Leverage</option>
            <option value="0.5X">0.5X</option>
            <option value="1.0X">1.0X</option>
            <option value="1.5X">1.5X</option>
            <option value="2.0X">2.0X</option>
            <option value="5X">5X</option>
            <option value="10X">10X</option>
          </select>
        </div>

        <base-button :loading="loading" style="  background-color: #5d78ff;border: 1px solid #5d78ff;">Place Trade</base-button>
      </form>
    </div>

    <div v-show="this.screen1 === 'CFD'"  class="separate">


      <div id="tradingview_512a5-wrapper"
           style="position: relative;
               box-sizing: content-box;
               width: 98%;
               display: block;
               margin-left: auto;
               margin-right: auto;
               height: 560px;"
      >
        <iframe title="advanced chart TradingView widget" lang="en" id="tradingview_512a5" frameborder="0" allowtransparency="true" scrolling="no" allowfullscreen="true" src="https://s.tradingview.com/widgetembed/?hideideas=1&amp;overrides=%7B%7D&amp;enabled_features=%5B%5D&amp;disabled_features=%5B%5D&amp;locale=en#%7B%22symbol%22%3A%22FX%3AUSDOLLAR%22%2C%22frameElementId%22%3A%22tradingview_512a5%22%2C%22interval%22%3A%22D%22%2C%22hide_side_toolbar%22%3A%220%22%2C%22allow_symbol_change%22%3A%221%22%2C%22save_image%22%3A%221%22%2C%22studies%22%3A%22%5B%5D%22%2C%22theme%22%3A%22dark%22%2C%22style%22%3A%221%22%2C%22timezone%22%3A%22Etc%2FUTC%22%2C%22withdateranges%22%3A%221%22%2C%22show_popup_button%22%3A%221%22%2C%22studies_overrides%22%3A%22%7B%7D%22%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22chart%22%2C%22utm_term%22%3A%22FX%3AUSDOLLAR%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeCFD%22%7D" style="width: 100%; height: 100%; margin: 0px !important; padding: 0px !important;"></iframe>
      </div>

      <form ref="myForm" class="form-part" @submit.prevent="placeTrade">

        <div class="form-header">
          <p style="font-weight: bold;color: #FFFFFF;">TRADE CFD - PLACE TRADE</p>
        </div>

        <div class="form-group">
          <label class="label">Amount</label>
          <input type="number" placeholder="Enter Amount"  name="Amount" v-model="amountTrade" required/>
        </div>

        <div class="form-group">
          <label class="label">Trading Pair</label>
          <select name="tradingPair" id="tradingPair" required v-model="symbolTraded" >
            <option selected disabled value="">Choose Trading Pair</option>
            <option :value="null" disabled>Choose Trading Pair</option>
            <option value="US 30">US 30</option>
            <option value="UKX">UKX</option>
            <option value="VIX Volatility Index">VIX Volatility Index</option>
            <option value="Germany 30">Germany 30</option>
            <option value="USA 500">USA 500</option>
            <option value="US Tech 100">US Tech 100</option>
            <option value="Japan 225">Japan 225</option>
            <option value="Europe 50">Europe 50</option>
            <option value="US Wall St 30">US Wall St 30</option>
            <option value="AUXAUD">AUXAUD</option>
            <option value="BCOUSD">BCOUSD</option>
            <option value="WEST TEXAS OIL">WEST TEXAS OIL</option>
            <option value="CAC40">CAC40</option>
            <option value="DXY">DXY</option>
            <option value="EU50">EU50</option>
            <option value="FR40">FR40</option>
            <option value="GRXEUR">GRXEUR</option>
            <option value="HELCHF">HELCHF</option>
            <option value="JPXJPY">JPXJPY</option>
            <option value="KRUUSD">KRUUSD</option>
            <option value="LTNEUR">LTNEUR</option>
            <option value="RUA">RUA</option>
            <option value="TR03">TR03</option>
            <option value="USDBRO">USDBRO</option>
            <option value="S&amp;P 100">S&amp;P 100</option>
            <option value="SXE5">SXE5</option>
            <option value="DOECHF">DOECHF</option>
            <option value="FAANG">FAANG</option>
            <option value="GRXEUR">GRXEUR</option>
            <option value="VRLCHF">VRLCHF</option>
            <option value="XPTUSD">XPTUSD</option>
            <option value="ZA20">ZA20</option>
            <option value="HK50">HK50</option>
            <option value="ID05Y">ID05Y</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Interval (Time)</label>
          <select name="tradeInterval" id="tradeInterval" required v-model="tradeTime">
            <option selected disabled value="">Trade Interval (Time)</option>
            <option :value="null" disabled>Trade Interval (Time)</option>
            <option value="1 min">1 min</option>
            <option value="3 min">3 min</option>
            <option value="5 min">5 min</option>
            <option value="15 mins">15 mins</option>
            <option value="30 mins">30 mins</option>
            <option value="1 hr">1 hr</option>
            <option value="2 hr">2 hr</option>
            <option value="1 day">1 day</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Type</label>
          <select name="tradeType" id="tradeType" required v-model="tradeType" >
            <option selected disabled value="">Trade Type</option>
            <option :value="null" disabled>Trade Type</option>
            <option value="Buy">Buy</option>
            <option value="Sell">Sell</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Leverage</label>
          <select name="tradeLeverage" id="tradeLeverage" required v-model="leverage" >
            <option selected disabled value="">Trade Leverage</option>
            <option :value="null" disabled>Trade Leverage</option>
            <option value="0.5X">0.5X</option>
            <option value="1.0X">1.0X</option>
            <option value="1.5X">1.5X</option>
            <option value="2.0X">2.0X</option>
            <option value="5X">5X</option>
            <option value="10X">10X</option>
          </select>
        </div>

        <base-button :loading="loading" style="  background-color: #5d78ff;border: 1px solid #5d78ff;">Place Trade</base-button>
      </form>
    </div>

    <div v-show="this.screen1 === 'Stocks'"  class="separate">

          <div id="tradingview_a28b8-wrapper"
               style="position: relative;
               box-sizing: content-box;
               width: 98%;
               display: block;
               margin-left: auto;
               margin-right: auto;
               height: 560px;"
          >
            <iframe title="advanced chart TradingView widget" lang="en" id="tradingview_a28b8" frameborder="0" allowtransparency="true" scrolling="no" allowfullscreen="true" src="https://s.tradingview.com/widgetembed/?hideideas=1&amp;overrides=%7B%7D&amp;enabled_features=%5B%5D&amp;disabled_features=%5B%5D&amp;locale=en#%7B%22symbol%22%3A%22NYSE%3ASPXC%22%2C%22frameElementId%22%3A%22tradingview_a28b8%22%2C%22interval%22%3A%22D%22%2C%22hide_side_toolbar%22%3A%220%22%2C%22allow_symbol_change%22%3A%221%22%2C%22save_image%22%3A%221%22%2C%22studies%22%3A%22%5B%5D%22%2C%22theme%22%3A%22dark%22%2C%22style%22%3A%221%22%2C%22timezone%22%3A%22Etc%2FUTC%22%2C%22withdateranges%22%3A%221%22%2C%22show_popup_button%22%3A%221%22%2C%22studies_overrides%22%3A%22%7B%7D%22%2C%22utm_source%22%3A%22infiniteprotrades.com%22%2C%22utm_medium%22%3A%22widget%22%2C%22utm_campaign%22%3A%22chart%22%2C%22utm_term%22%3A%22NYSE%3ASPXC%22%2C%22page-uri%22%3A%22infiniteprotrades.com%2Findex.php%2Fuser%2FtradeStocks%22%7D" style="width: 100%; height: 100%; margin: 0px !important; padding: 0px !important;"></iframe>
          </div>

      <form ref="myForm" class="form-part" @submit.prevent="placeTrade">

        <div class="form-header">
          <p style="font-weight: bold;color: #FFFFFF;">TRADE STOCKS - PLACE TRADE</p>
        </div>

        <div class="form-group">
          <label class="label">Amount</label>
          <input type="number" placeholder="Enter Amount"  name="Amount" v-model="amountTrade" required/>
        </div>

        <div class="form-group">
          <label class="label">Trading Pair</label>
          <select name="tradingPair" id="tradingPair" required v-model="symbolTraded" >
            <option selected disabled value="">Choose Trading Pair</option>
            <option :value="null" disabled>Choose Trading Pair</option>
            <option value="AMAZON">AMAZON</option>
            <option value="APPLE">APPLE</option>
            <option value="COCA COLA">COCA COLA</option>
            <option value="DAX30">DAX30</option>
            <option value="AIRBNB INC">AIRBNB INC</option>
            <option value="BOEING CO">BOEING CO</option>
            <option value="GME STOCKS">GME STOCKS</option>
            <option value="AMC ENTERTAINMENT">AMC ENTERTAINMENT</option>
            <option value="BLACKBERRY">BLACKBERRY</option>
            <option value="CITIGROUP INC">CITIGROUP INC</option>
            <option value="CISCO SYSTEMS INC">CISCO SYSTEMS INC</option>
            <option value="FACEBOOK">FACEBOOK</option>
            <option value="TWITTER">TWITTER</option>
            <option value="TESLA INC">TESLA INC</option>
            <option value="SONY ENT">SONY ENT</option>
            <option value="NASDAQ">NASDAQ</option>
            <option value="ENTERPRISE GROUP INC">ENTERPRISE GROUP INC</option>
            <option value="FORD MOTOR">FORD MOTOR</option>
            <option value="GAZPROM">GAZPROM</option>
            <option value="GLOBE LIFE INC">GLOBE LIFE INC</option>
            <option value="HYDRO ONE LTD">HYDRO ONE LTD</option>
            <option value="LOTUS VENTURES INC">LOTUS VENTURES INC</option>
            <option value="KELLOGG COMPANY">KELLOGG COMPANY</option>
            <option value="WAYFAIR INC">WAYFAIR INC</option>
            <option value="WALMART INC">WALMART INC</option>
            <option value="WALT DISNEY CO">WALT DISNEY CO</option>
            <option value="MACY'S INC">MACY'S INC</option>
            <option value="MCDONALD'S CORPORATIONS">MCDONALD'S CORPORATIONS</option>
            <option value="VISA INC">VISA INC</option>
            <option value="VERIZON">VERIZON</option>
            <option value="TMX GROUP LTD">TMX GROUP LTD</option>
            <option value="ALPHABET INC">ALPHABET INC</option>
            <option value="ORGANIGRAM HOLDINGS">ORGANIGRAM HOLDINGS</option>
            <option value="PFIZER INC">PFIZER INC</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Interval (Time)</label>
          <select name="tradeInterval" id="tradeInterval" required v-model="tradeTime" >
            <option selected disabled value="">Trade Interval (Time)</option>
            <option :value="null" disabled>Trade Interval (Time)</option>
            <option value="1 min">1 min</option>
            <option value="3 min">3 min</option>
            <option value="5 min">5 min</option>
            <option value="15 mins">15 mins</option>
            <option value="30 mins">30 mins</option>
            <option value="1 hr">1 hr</option>
            <option value="2 hr">2 hr</option>
            <option value="1 day">1 day</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Type</label>
          <select name="tradeType" id="tradeType" required v-model="tradeType">
            <option selected disabled value="">Trade Type</option>
            <option :value="null" disabled>Trade Type</option>
            <option value="Buy">Buy</option>
            <option value="Sell">Sell</option>
          </select>
        </div>

        <div class="form-group">
          <label class="label">Trade Leverage</label>
          <select name="tradeLeverage" id="tradeLeverage" required v-model="leverage" >
            <option selected disabled value="">Trade Leverage</option>
            <option :value="null" disabled>Trade Leverage</option>
            <option value="0.5X">0.5X</option>
            <option value="1.0X">1.0X</option>
            <option value="1.5X">1.5X</option>
            <option value="2.0X">2.0X</option>
            <option value="5X">5X</option>
            <option value="10X">10X</option>
          </select>
        </div>

        <base-button :loading="loading" style="  background-color: #5d78ff;border: 1px solid #5d78ff;">Place Trade </base-button>
      </form>
    </div>


    <div class="last">
      <div class="body">
        <h2>My trade history</h2>
        <div class="row trans-mgt">
          <div class="form-group fg--search">
<!--            <button type="submit"><i class="fa fa-search"></i></button>-->
            <input type="text" class="input" placeholder="Search..."/>
          </div>
          <div class="row filter_group">
            <!--          <div class="blue">Download transactions</div>-->
            <div class="action-content">
              <img src="@/assets/Filterslines.svg"  alt="Export"/>
              <p>Filter</p>
            </div>
          </div>
        </div>
      </div>
      <div class="section-5">

        <div class="empty-state-container" v-if="this.readUserTrade.trades.length === 0">
          <img src="@/assets/empty.svg" alt="empty" class="empty-state">
          <p style="text-align: center;color: #FFFFFF; font-size: 13px;padding-bottom: 3px;" class="empty-state-text-1">You have nothing to see</p>
          <p style="text-align: center;color: #FFFFFF; font-size: 13px;padding-bottom: 3px;" class="empty-state-text-2">This is where your Trade history will appear</p>
          <!--        <p class="empty-state-text-3">-->
          <!--          <i class='bx bx-plus' ></i>-->
          <!--          Transaction-->
          <!--        </p>-->
        </div>

        <div class="table" v-if="this.readUserTrade.trades.length > 0" >
          <table>
            <tr style="background-color: #FFFFFF;">
              <th>Trade ID</th>
              <th>Trade Type</th>
              <th>Trade Time</th>
              <th>Symbol Traded</th>
              <th>Expected Payout</th>
              <th>Leverage</th>
              <th>End Price</th>
              <th>End Time</th>
              <th>Trade Status</th>
            </tr>

            <tbody v-for="child in paginatedItems" :key="child.key">
            <tr>
              <td data-label="Trade ID">{{child.tradeReference}}</td>
              <td data-label="Trade Type">{{child.tradeType}}</td>
              <td data-label="Trade Time">{{child.tradeTime | formatDate2}}</td>
              <td data-label="Symbol Traded">{{child.symbolTraded}}</td>
              <td data-label="Expected Payout">
                <div v-if="child.tradeStatus === 'won'" class="table-sep">
                  <i v-if="child.tradeType === 'Buy'" style="color: #10d876 !important" class="fa fa-arrow-up text-success"></i>
                  <i v-if="child.tradeType === 'Sell'" style="color: #E50202 !important" class="fa fa-arrow-down text-danger"></i>
                  <p>{{child.expectedPayout}}</p>
                </div>
                <div v-if="child.tradeStatus === 'lost'" class="table-sep">
                  <i v-if="child.tradeType === 'Buy'" style="color: #10d876 !important" class="fa fa-arrow-up text-success"></i>
                  <i v-if="child.tradeType === 'Sell'" style="color: #E50202 !important" class="fa fa-arrow-down text-danger"></i>
                  <p>{{child.expectedPayout}}</p>
                </div>
                <div v-if="child.tradeStatus === 'pending'" class="table-sep">
                  <i v-if="child.tradeType === 'Buy'" style="color: #10d876 !important" class="fa fa-arrow-up text-success"></i>
                  <i v-if="child.tradeType === 'Sell'" style="color: #E50202 !important" class="fa fa-arrow-down text-danger"></i>
                  <p style="font-size: 12px;">$ PendingTrade</p>
                </div>
              </td>
              <td data-label="Leverage">{{child.leverage}}</td>
              <td data-label="End Price">{{child.endPrice}}</td>
              <td data-label="End Time">{{child.endTime | formatDate}}</td>
              <td data-label="Trade Status">
                <div>
                  <p class="status-won" v-show="child.tradeStatus === 'won'">{{child.tradeStatus}}</p>
                  <p class="status-lost" v-show="child.tradeStatus === 'lost'">{{child.tradeStatus}}</p>
                  <p class="status-pending" v-show="child.tradeStatus === 'pending'">{{child.tradeStatus}}</p>
                </div>
              </td>
            </tr>
            </tbody>
          </table>

          <div class="pagination">
            <button @click="previousPage" :disabled="currentPage === 1" class="previous">Previous</button>
            <div class="page-indicator">
              Page {{ currentPage }} of {{ totalPages }}
            </div>
            <button @click="nextPage" :disabled="currentPage === totalPages" class="previous">Next</button>
          </div>
        </div>
      </div>
    </div>
    </div>

</template>

<script>
import BaseButton from "@/components/BaseComponents/buttons/BaseButton.vue";
import StoreUtils from "@/utility/StoreUtils";
import TradeRequest from "@/model/request/TradeRequest";
import {mapState} from "vuex";
// import axios from "axios";

export default {
  name: "DashBoardOverView",
  components: {BaseButton},
  data () {
    return {
      model: new TradeRequest().createTrade,
      history: [],
      currentPage: 1,
      itemsPerPage: 10,
      screen1: "Forex",
      screen2: "Crypto",
      screen3: "CFD",
      screen4: "Stocks",
      userId: "",
      userInfo: "",
      currentDate: "",
      currentDate2: "",
      randomString: "",
      randomString2: "",
      amountTrade: "",
      symbolTraded: "",
      tradeTime: "",
      tradeType: "",
      leverage: "",

      dollars: 0,
      bitcoin: null,
      // bitcoinRate: null,
    }
  },
  computed:{
    paginatedItems() {
      const startIndex = (this.currentPage - 1) * this.itemsPerPage;
      const endIndex = startIndex + this.itemsPerPage;
      return this.readUserTrade.trades.slice(startIndex, endIndex);
    },
    totalPages() {
      return Math.ceil(this.readUserTrade.trades.length / this.itemsPerPage);
    },
    UserInfo() {
      return StoreUtils.rootGetters(StoreUtils.getters.auth.getUserInfo)
    },
    UserDetails() {
      return StoreUtils.rootGetters(StoreUtils.getters.auth.getReadUserById)
    },
    // readUserTrade() {
    //   return StoreUtils.rootGetters(StoreUtils.getters.trade.getReadUserTrade)
    // },
    ...mapState({
      loading: state => state.trade.loading,
      auth: state => state.auth,
      readUserTrade: state => state.trade.readUserTrade,
      bitcoinRate: state => state.auth.bitcoinRate,
    }),
  },

  methods: {
    // fetchBitcoinRate() {
    //   axios.get('https://api.coindesk.com/v1/bpi/currentprice/BTC.json')
    //       .then(response => {
    //         this.bitcoinRate = response.data.bpi.USD.rate_float;
    //       })
    //       .catch(error => console.error(error));
    // },
    convertToBitcoin() {
      if (!this.bitcoinRate.bitcoinRate) {
        alert('Bitcoin rate not loaded. Please wait or try reloading the page.');
        return;
      }
      this.bitcoin = (this.UserDetails.user.totalDepositedAmount / this.bitcoinRate.bitcoinRate).toFixed(8);
    },
    onPostClick() {
      this.$router.push("/fund-wallet");
    },
    onPostClick2() {
      this.$router.push("/withdrawal");
    },
    previousPage() {
      if (this.currentPage > 1) {
        this.currentPage--;
      }
    },
    nextPage() {
      if (this.currentPage < this.totalPages) {
        this.currentPage++;
      }
    },
    goToPage(pageNumber) {
      if (pageNumber > 0 && pageNumber <= this.totalPages) {
        this.currentPage = pageNumber;
      }
    },
    toggleScreen() {
      this.screen1 = "Forex"
    },
    toggleScreen2() {
      this.screen1 = this.screen2
    },
    toggleScreen3() {
      this.screen1 = this.screen3
    },
    toggleScreen4() {
      this.screen1 = this.screen4
    },

    async placeTrade() {
      await StoreUtils.dispatch(StoreUtils.actions.trade.tradeCreate, {
        userId: this.userId,
        tradeTime: this.currentDate,
        symbolTraded: this.symbolTraded,
        amountTrade: this.amountTrade,
        expectedPayout: 0,
        leverage: this.leverage,
        endPrice: this.randomString2,
        marketType: this.screen1,
        endTime: this.currentDate2,
        tradeStatus: "pending",
        tradeReference : this.randomString,
        tradeType : this.tradeType
      });
      await StoreUtils.dispatch(StoreUtils.actions.trade.readUserTrade, {
        userId: localStorage.getItem('userId'),
      });
      this.getCurrentDate();
      this.getCurrentDateTime();
      this.generateRandomString();
      this.generateRandomString2();
    },

    getCurrentDate() {
      const today = new Date();

      // Format the date as needed, for example: YYYY-MM-DD
      const formattedDate = today.toISOString().split('T')[0];

      // Save the formatted date to the data property
      this.currentDate2 = formattedDate;
    },


    getCurrentDateTime() {
      const today = new Date();

      // Format the date as YYYY-MM-DD HH:mm:ss
      const formattedDateTime = today.toISOString().slice(0, 19).replace("T", " ");

      // Save the formatted date and time to the data property
      this.currentDate = formattedDateTime;
    },

    generateRandomString() {
      const characters = '0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz';
      let result = '';
      for (let i = 0; i < 10; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        result += characters.charAt(randomIndex);
      }
      this.randomString = result;
    },

    generateRandomString2() {
      const characters = '0123456789';
      let result = '';
      for (let i = 0; i < 4; i++) {
        const randomIndex = Math.floor(Math.random() * characters.length);
        result += characters.charAt(randomIndex);
      }
      this.randomString2 = result;
    }
  },

  created() {
    this.getCurrentDate();
    this.getCurrentDateTime();
    this.generateRandomString();
    this.generateRandomString2();
    this.convertToBitcoin();

    StoreUtils.rootGetters(StoreUtils.getters.auth.getBitcoinRate)

    StoreUtils.rootGetters(StoreUtils.getters.trade.getReadUserTrade)

    StoreUtils.dispatch(StoreUtils.actions.trade.readUserTrade, {
      userId : localStorage.getItem('userId'),
    });

    StoreUtils.dispatch(StoreUtils.actions.auth.readReadUserById, {
      userId : localStorage.getItem('userId')
    })

    StoreUtils.rootGetters(StoreUtils.getters.auth.getReadUserById)

    this.userId = localStorage.getItem('userId')

    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  },

  mounted() {
    this.getCurrentDate();
    this.getCurrentDateTime();
    this.generateRandomString();
    this.generateRandomString2();
    this.convertToBitcoin();

    StoreUtils.rootGetters(StoreUtils.getters.auth.getBitcoinRate)

    StoreUtils.rootGetters(StoreUtils.getters.trade.getReadUserTrade)

    StoreUtils.dispatch(StoreUtils.actions.trade.readUserTrade, {
      userId : localStorage.getItem('userId'),
    });

    StoreUtils.dispatch(StoreUtils.actions.auth.readReadUserById, {
      userId : localStorage.getItem('userId')
    })

    StoreUtils.rootGetters(StoreUtils.getters.auth.getReadUserById)

    this.userId = localStorage.getItem('userId')

    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  }

}
</script>

<style scoped>
.text-2{
  color: #770101;
  background-color: #facccc;
  border-color: #f8b8b8;
  position: relative;
  padding: 0.75rem 1.25rem;
  margin-bottom: 0.5rem;
  border-radius: 0.25rem;
}
.status-pending{
  background-color: #FE9431;
  border-radius: 5px;
  font-size: 12px;
  width: 70px;
  padding: 2px 5px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.status-won{
  background-color: #10d876;
  border-radius: 5px;
  font-size: 12px;
  width: 70px;
  padding: 2px 5px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.status-lost{
  background-color: #E50202;
  border-radius: 5px;
  font-size: 12px;
  width: 70px;
  padding: 2px 5px;
  display: block;
  margin-left: auto;
  margin-right: auto;
}
i{
  font-size: 13px;
}
.table-sep{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  gap: 5px;
}
.empty-state-container{
  display: block;
  margin-left: auto;
  margin-right: auto;
  width: 30%;
}
.empty-state{
  display: block;
  margin-left: auto;
  margin-right: auto;
}
.lawrence{
  display: flex;
  gap: 20px;
}
.section-2{
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  padding-right: 3%;
  padding-left: 1.5%;
  margin-top: 1.5%;
  margin-bottom: 1.5%;
}
.section-2-part-1{
  display: flex;
  align-content: center;
  align-items: center;
  gap: 10px;
}

.trade-btn-1{
  padding: 8px 14px;
  text-align: center;
  font-size: 12px;
  width: 125px;
  height: 30px;
  background: #E50202;
  color: #ffffff;
  border: 1px solid #E50202;
  border-radius: 4px;
}

.trade-btn-1:hover{
  box-shadow: 0px 1px 10px rgba(16, 24, 40, 1);
}

.trade-btn-2{
  padding: 8px 14px;
  text-align: center;
  font-size: 12px;
  width: 125px;
  height: 30px;
  background: #10d876;
  color: #ffffff;
  border: 1px solid #10d876;
  border-radius: 4px;
}

.trade-btn-2:hover{
  box-shadow: 0px 1px 10px rgba(16, 24, 40, 1);
}

.trade-btn-3{
  padding: 8px 14px;
  text-align: center;
  font-size: 12px;
  width: 125px;
  height: 30px;
  background: #FE9431;
  color: #ffffff;
  border: 1px solid #FE9431;
  border-radius: 4px;
}

.trade-btn-3:hover{
  box-shadow: 0px 1px 10px rgba(16, 24, 40, 1);
}

.trade-btn-4{
  padding: 8px 14px;
  text-align: center;
  font-size: 12px;
  width: 125px;
  height: 30px;
  background: #5d78ff;
  color: #ffffff;
  border: 1px solid #5d78ff;
  border-radius: 4px;
}

.trade-btn-4:hover{
  box-shadow: 0px 1px 10px rgba(16, 24, 40, 1);
}

.form-header{
  padding-top: 5px;
  padding-bottom: 15px;
}

.fund-wallet{
  display: flex;
  align-content: center;
  align-items: center;
  padding: 8px 14px;
  gap: 8px;
  font-size: 12px;
  width: 125px;
  height: 30px;
  background: #0f171c;
  color: #ffffff;
  border: 0.5px solid #3C4A57FF;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 4px;
  margin-right: 3%;
}

.fund-wallet:hover{
  background: #ffcf01;
  color: #ffffff;
  border: 1px solid #ffcf01;
  /*box-shadow: 0 0 5px rgba(0, 0, 0, 0.4);*/
}

.section-2-part-2{
  display: flex;
  align-content: center;
  align-items: center;
}


.section-3{
  display: flex;
  align-content: center;
  align-items: center;
  padding: 15px 25px;
  gap: 24px;
  width: 1183px;
  height: 110px;
  background: #0f171c;
  border: 0.5px solid #3C4A57FF;
  border-radius: 4px;
  margin-left: 0.5%;
}

.section-3-content{
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  width: 20%;
}

.vl-2{
  border-left: 1px solid #E7E8F0;
  height: 50px;
  margin-left: 1%;
  margin-right: 1%;
}

.content-1-text-1{
  font-weight: 600;
  font-size: 15px;
  line-height: 18px;
  letter-spacing: 0.02em;
  color: #ffffff;
}

.content-1-text-2{
  font-weight: 600;
  font-size: 18px;
  line-height: 30px;
  display: flex;
  align-items: center;
  color: #ffffff;
}

.separate{
  display: flex;
  justify-content: space-between;
  align-content: center;
  align-items: center;
  margin-right: 3%;
  margin-top: 1%;
  margin-bottom: 1%;
}

.form-group {
  margin-bottom: 15px;
}

.form-group input {
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 15px;
  line-height: 24px;
  letter-spacing: -0.1px;
  padding: 13px 16px;
  height: 35px;
  border: 0.5px solid #3C4A57FF;
  box-shadow: none;
  width: 500px;
  background: #FFFFFF;
  margin-top: 1.5%;
  color: #667085;
}

.form-group input:focus {
  outline: none;
}

.form-group input::placeholder {
  color: var(--black-color);
  font-weight: 400;
  font-size: 14px;
}

.form-group select {
  display: block;
  margin-left: auto;
  margin-right: auto;
  font-size: 15px;
  line-height: 24px;
  letter-spacing: -0.1px;
  padding: 13px 16px;
  height: 45px;
  border-radius: 8px;
  border: 0.5px solid #3C4A57FF;
  box-shadow: none;
  width: 500px;
  background: #FFFFFF;
  margin-top: 1.5%;
  color: #667085;
}

option{
  color: #667085;
}

.form-group select:focus {
  outline: none;
}

.form-group select::placeholder {
  color: var(--black-color);
  font-weight: 400;
  font-size: 14px;
}

.form-part{
  max-width: 580px;
  width: 70%;
  margin: auto;
  border: 0.5px solid #3C4A57FF;
  padding: 22px 25px;
  border-radius: 5px;
  background: #0f171c;
}

.label{
  margin-left: 3%;
  font-size: 14px;
  color: #FFFFFF;
}

.body{
  margin-right: 3%;
  margin-left: 2%;
}

h2{
  font-weight: 700;
  font-size: 17px;
  line-height: 25px;
  color: #ffffff;
  margin-left: 1.5%;
}
.row{
  display: flex;
  align-content: center;
  align-items: center;
}
.trans-mgt{
  /*margin-top: 17px;*/
  /* align-items: center; */
}
.filter_group{
  margin-left: auto;
  gap: 16px;
}


.fg--search {
  background: none;
  position: relative;
  width: 400px;
  margin-left: 1%;
}
.fg--search input {
  width: 100%;
  padding: 10px;
  padding-left: 15px;
  display: block;
  background: #0f171c;
  border: 0.5px solid #3C4A57FF;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 6px;
  color: #FFFFFF;
}

.fg--search button {
  background: transparent;
  border: none;
  cursor: pointer;
  display: inline-block;
  font-size: 10px;
  position: absolute;
  top: 0;
  right: 0;
  padding: 10px;
  margin-top: 5px;
}

table {
  border-collapse: collapse;
  width: 100%;
  /*margin-top: 10px;*/
}
.table{
  margin-left: 3%;
  margin-right: 4%;
  margin-bottom: 1%;
}

tr{
  border: 0.5px solid #3C4A57FF;
}

th {
  background-color: #0f171c;
  padding: 10px;
  letter-spacing: 0.5px;
  font-weight: 500;
  font-size: 12px;
  color: #ffffff;
  text-align: center;
}

td {
  /*border: 1px solid #E3EBF6;*/
  text-align: center;
  align-items: center;
  align-content: center;
  padding: 12px 8px;
  /*letter-spacing: 1px;*/
  color: #ffffff;
  font-weight: 200;
  font-size: 12px;
  /*border-bottom: 1px solid #E3EBF6;*/
}

.action-content{
  display: flex;
  align-items: center;
  align-content: center;
  padding: 8px 14px;
  gap: 8px;
  width: 88px;
  height: 36px;
  background: #0f171c;
  border: 0.5px solid #3C4A57FF;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 4px;
  margin-right: 13px;
}

.action-content:hover{
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
}

.action-content p {
  color: #ffffff;
  font-size: 13px;
}

/*tr td:first-child:before*/
/*{*/
/*  counter-increment: Serial;      !* Increment the Serial counter *!*/
/*  content:counter(Serial); !* Display the counter *!*/
/*}*/

.pagination{
  display: flex;
  align-content: center;
  align-items: center;
  justify-content: space-between;
  padding-top: 8px;
}

.previous{
  /*display: flex;*/
  /*align-content: center;*/
  /*align-items: center;*/
  text-align: center;
  padding: 8px 14px;
  gap: 8px;
  font-size: 12px;
  width: 100px;
  height: 30px;
  background: transparent;
  color: #ffffff;
  /*border: 1px solid #1570EF;*/
  border: 0.5px solid #3C4A57FF;
  box-shadow: 0 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 4px;
}

.previous:hover{
  box-shadow: 0 0 5px rgba(16, 24, 40, 0.2);
}

.page-indicator{
  color: #ffffff;
  font-weight: 200;
  font-size: 13px;
}

.tradingview_7a2ab-wrapper{
  position: relative;
  box-sizing: content-box;
  margin: 0px auto !important;
  padding: 0px !important;
  width: 580px;
  height: 570px;
}



@media (max-width: 700px) {

  .fund-wallet{
    display: none;
  }

  .section-3{
    display: flex;
    align-content: center;
    align-items: center;
    padding: 15px 10px;
    gap: 24px;
    width: 100%;
    height: 100%;
    margin-left: unset;
    margin-bottom: 2%;
  }

  .form-part {
    max-width: 615px;
    width: 100%;
    padding: 22px 25px;
    margin-top: 5%;
  }

  .law{
    margin-right: 1%;
  }

  .content-1-text-1{
    font-size: 12px;
    width: 100%;
  }

  .content-1-text-2{
    font-size: 13px;
  }

  .separate{
    display: block;
    margin-right: unset;
    margin-left: unset;
    margin-top: 1%;
    margin-bottom: 1%;
  }

  .form-group input {
    width: 100%;
  }


  .form-group select {
    width: 100%;
  }

  .tradingview_7a2ab-wrapper{
    width: 90%;
    display: block;
    margin-right: auto;
    margin-left: auto;
  }

  .last{
    margin-top: 4%;
  }

  h2{
    font-size: 15px;
  }

  .lawrence{
    gap: 10px;
  }

  .trade-btn-1{
    width: 110px;
    height: 33px;
  }

  .trade-btn-2{
    width: 110px;
    height: 33px;
  }

  .trade-btn-3{
    width: 110px;
    height: 33px;
  }

  .trade-btn-4{
    width: 110px;
    height: 33px;
  }

  th {
    display: none;
  }

  table, thead, tbody, td, tr {
    display: block;
  }

  thead tr {
    position: absolute;
    top: -9999px;
    left: -9999px;
  }

  tr {
    border: 0.5px solid #ccc;
  }

  td {
    /* Each cell is now a full-width row */
    border: none;
    position: relative;
    padding-left: 60%;
    text-align: center;
    margin-bottom: 10px;
    font-size: 15px;
  }

  td:before {
    /* Use the data-label for the pseudo-element content */
    content: attr(data-label);
    position: absolute;
    left: 10px;
    padding-left: 5%;
    font-weight: bold;
  }

}

@media (max-width: 500px) {
  .trade-btn-1{
    width: 90px;
    height: 30px;
    font-size: 9px;
  }

  .trade-btn-2{
    width: 90px;
    height: 30px;
    font-size: 9px;
  }

  .trade-btn-3{
    width: 90px;
    height: 30px;
    font-size: 9px;
  }

  .trade-btn-4{
    width: 90px;
    height: 30px;
    font-size: 9px;
  }

  .vl-2{
    display: none;
  }

  .section-3{
    display: block;
    padding: 20px 20px;
    gap: 30px;
    width: 100%;
    height: 100%;
    margin-left: unset;
  }

  .section-3-content{
    display: flex;
    justify-content: space-between;
    width: 100%;
    margin-bottom: 10px;
  }

  .content-1-text-1{
    font-weight: 900;
    font-size: 16px;
  }

  .content-1-text-2{
    font-weight: 300;
    font-size: 14px;
    line-height: 30px;
  }

  .form-part{
    max-width: unset;
    width: 97%;
    margin-top: 5%;
    display: block;
    margin-right: auto;
    margin-left: auto;
  }
  .filter_group{
    display: none;
  }

  .lawrence{
    gap: 5px;
  }

  .section-2-part-1{
    gap: 5px;
  }

  .empty-state-container{
    display: block;
    margin-left: auto;
    margin-right: auto;
    width: 90%;
  }

  .empty-state{
    width: 35%;
  }

}

</style>