<template>
  <div class="container">
    <h2>Search</h2>
    <div class="row">
      <div class="col-12 col-sm-6 col-md-6 col-lg-6 col-xl-6">
        <select
          class="productSelect"
          name="productSelect"
          id="productSelect"
          v-model="selectedData"
        >
          <option
            v-for="(obj, key) in dropDownData"
            :key="key"
            v-bind:value="obj"
          >{{obj.product_name}}</option>
        </select>
        <button class="search" v-on:click="composeURL">Search</button>
      </div>
      <div class="col-12 col-sm-6 col-md-6 col-lg-6 col-xl-6 right">
        <div class="result">
          <a :href="resultUrl">{{resultUrl}}</a>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from "axios";

export default {
  name: "MainComponent",
  created() {
    this.sortDatesArray();
  },
  data() {
    return {
      datesArray: [
        { date: "10.01.2017" },
        { date: "05.11.2016" },
        { date: "21.13.2002" }
      ],
      dropDownData: [],
      selectedData: {},
      resultUrl: ""
    };
  },
  mounted() {
    axios({
      method: "GET",
      url:
        "https://cors-anywhere.herokuapp.com/https://www.acronis.com/en-us/api/v1/price/?machine_name=acronis_backup&locale=en-us"
    }).then(
      result => {
        const dataObj = result.data[0].subscription.buy;
        for (const item in dataObj) {
          this.dropDownData.push(dataObj[item]);
        }
      },
      error => {
        console.error(error);
      }
    );
  },
  methods: {
    sortDatesArray: function() {
      const sortedArray = this.datesArray.sort(
        (a, b) => new Date(a).valueOf() - new Date(b.valueOf())
      );
      console.warn(sortedArray);
      return sortedArray;
    },
    composeURL() {
      this.resultUrl = `https://store.acronis.com/${this.selectedData.store}/purl-consumer-standard-US?cart=${this.selectedData.cb_id}&currencies=${this.selectedData.currency}`;
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.container {
  text-align: center;
}
h2 {
  margin-bottom: 20px;
}
.col-6 {
  text-align: right;
}
.right {
  text-align: left;
}
.btn {
  width: 100%;
  height: 45px;
  border: 1px solid black;
  border-radius: 5px;
  text-align: left;
  padding: 0 0 0 10px;
}
.btn-text {
  position: relative;
  top: 10px;
}
.icon {
  float: right;
  background-color: #f2f2f2;
  height: 43px;
  border-top-right-radius: 5px;
  border-bottom-right-radius: 5px;
  border-left: 1px solid black;
  width: 7%;
  text-align: center;
}
img {
  width: 20px;
  position: relative;
  top: 10px;
}
.result {
  width: 100%;
  height: 100px;
  border: 1px solid black;
  padding: 10px;
  text-align: left;
}
.search {
  margin: 20px 0 20px 0;
  font-size: 18px;
  width: 100%;
  border-radius: 5px;
}
.productSelect {
  width: 100%;
  height: 45px;
}
a:hover {
  text-decoration: none;
}
</style>
