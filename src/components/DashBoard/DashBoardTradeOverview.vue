<template>
  <div class="alpha">
    <div class="body">
      <h2>Trade Overview</h2>
      <div class="row trans-mgt">
        <div class="form-group fg--search">
          <button type="submit"><i class="fa fa-search"></i></button>
          <input type="text" class="input" placeholder="Search trades..."/>
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
      <div class="empty-state" v-if="this.readUserTrade.trades.length === 0">
        <img src="@/assets/empty.svg" alt="empty">
        <p class="empty-state-text-1">You have nothing to see</p>
        <p class="empty-state-text-2">This is where your Transactions will appear</p>
        <!--        <p class="empty-state-text-3">-->
        <!--          <i class='bx bx-plus' ></i>-->
        <!--          Transaction-->
        <!--        </p>-->
      </div>

      <div class="table" v-if="this.readUserTrade.trades.length > 0">
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
            <td>{{child.tradeReference}}</td>
            <td>{{child.tradeType}}</td>
            <td>{{child.tradeTime | formatDate2}}</td>
            <td>{{child.symbolTraded}}</td>
            <td>
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
                <p style="font-size: 12px;"> $ PendingTrade</p>
              </div>
            </td>
            <td>{{child.leverage}}</td>
            <td>{{child.endPrice}}</td>
            <td>{{child.endTime | formatDate}}</td>
            <td>
              <div>
                <p class="status-won" v-show="child.tradeStatus === 'won'" >{{child.tradeStatus}}</p>
                <p class="status-lost" v-show="child.tradeStatus === 'lost'" >{{child.tradeStatus}}</p>
                <p class="status-pending" v-show="child.tradeStatus === 'pending'" >{{child.tradeStatus}}</p>
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
</template>

<script>


import StoreUtils from "@/utility/StoreUtils";
import {mapState} from "vuex";

export default {
  name: "DashBoardTradeOverview",
  data () {
    return {
      history: [],
      investments: [],
      currentPage: 1,
      itemsPerPage: 10,
      userId: "",
      userInfo: "",
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
    ...mapState({
      loading: state => state.trade.loading,
      auth: state => state.auth,
      readUserTrade: state => state.trade.readUserTrade,
    }),
  },
  methods: {
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

  },

  created() {

    StoreUtils.rootGetters(StoreUtils.getters.trade.getReadUserTrade)


    this.userId = localStorage.getItem('userId')

    // Retrieve the object from local storage
    const storedObject = localStorage.getItem('userInfo');

    if (storedObject) {
      this.userInfo = JSON.parse(storedObject);
    }
  },

  mounted() {
    StoreUtils.dispatch(StoreUtils.actions.trade.readUserTrade, {
      userId : localStorage.getItem('userId'),
    });

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
.table-sep{
  display: flex;
  justify-content: center;
  align-content: center;
  align-items: center;
  gap: 5px;
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
.body{
  padding: 20px;
}
h2{
  font-weight: 700;
  font-size: 19px;
  line-height: 25px;
  color: #ffffff;
}
.row{
  display: flex;

}
.trans-mgt{
  margin-top: 17px;
  /* align-items: center; */
}
.filter_group{
  margin-left: auto;
  gap: 16px;
}

.white{
  display: flex;
  align-items: center;
  align-content: center;
  background-color: #FFFFFF;
  border: 0.5px solid #3C4A57FF;
  font-size: 13px;
  padding:  6px 14px;
  border-radius: 5px;
  gap: 10px;
}
.blue{
  display: flex;
  align-items: center;
  align-content: center;
  padding: 6px 14px;
  border-radius: 5px;
  font-size: 13px;
  background-color: #1570EF;
  border: 1px solid #1570EF;
  color: #ffffff;
}

.fg--search {
  background: none;
  position: relative;
  width: 400px;
  margin-left: 1%;
  color: #FFFFFF;
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

.fa-search{
  color: #667085;
  margin-right: 10px;
}
table {
  border-collapse: collapse;
  width: 100%;
  /*margin-top: 10px;*/
}
.table{
  margin-left: 2%;
  margin-right: 3%;
}

tr{
  border: 0.5px solid #3C4A57FF;
}

th {

  background-color: #0f171c;
  padding: 10px;
  letter-spacing: 0.5px;
  font-weight: 500;
  font-size: 13px;
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

.empty-state{
  text-align: center;
  margin-top: 7%;
  margin-right: 8%;
}


.empty-state-text-1{
  font-weight: 600;
  font-size: 18px;
  line-height: 20px;
  color: #ffffff;
  padding-top: 0.5%;
  padding-bottom: 0.5%;
}

.empty-state-text-2{
  font-weight: 200;
  font-size: 14px;
  line-height: 20px;
  text-align: center;
  color: #ffffff;
  padding-bottom: 1.25%;
}

.empty-state-text-3{
  display: flex;
  flex-direction: row;
  justify-content: center;
  align-items: center;
  padding: 10px 18px;
  gap: 8px;
  width: 130px;
  margin-right: auto;
  margin-left: auto;
  height: 35px;
  background: #0765FF;
  color: #FFFFFF;
  border: 1px solid #0765FF;
  box-shadow: 0px 1px 2px rgba(16, 24, 40, 0.05);
  border-radius: 5px;
  font-size: 13px;
}

.empty-state-text-3:hover{
  box-shadow: 0 0 5px rgba(0, 0, 0, 0.4);
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

input::placeholder{
  color: #FFFFFF;
}
@media (max-width: 500px) {
  .table{
    margin-left: unset;
  }
}

</style>