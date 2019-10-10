<template>
  <div class="about">
    <div class="top">
      <div class="container">
        <div class="row">
          <div class="col logo-top">
            <img src="/img/comviq-black.png" height="24" alt="COMVIQ LOGO" />
          </div>
          <div class="col top-link">ABONNEMANG</div>
          <div class="col top-link">KONTANTKORT</div>
          <div class="col top-link">MOBILER</div>
          <div class="col top-link">STUDENT</div>
          <div class="col top-link">UTLAND</div>
          <div class="col top-link">HJÄLP</div>
          <div class="col icons">
            <font-awesome-icon icon="search" />&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <font-awesome-icon icon="user" />
          </div>
          <div class="col">
            <div class="button-top">TANKA</div>
          </div>
        </div>
      </div>
    </div>
    <div class="top2">
      <div class="row">
        <div class="col">Tanka med Comviq</div>
      </div>
    </div>
    <div class="container">
      <div class="row greybox">
        <div class="round">1</div>Vilket nummer vill du tanka?
      </div>
      <div class="row whitebox">
        <div class="col">
          <input type="text" v-model="phonenumber" />
        </div>
        <div class="col-2 verified-button">verifierat</div>
      </div>
      <div class="row greybox">
        <div class="round">2</div>Vad vill du tanka?
      </div>
      <div class="row whitebox">
        <div class="col">
          <div class="amount" v-bind:class="{select: selectedopt == 1}">50 kr</div>
        </div>
        <div class="col">
          <div class="amount selected">100 kr</div>
        </div>
        <div class="col">
          <div class="amount">200 kr</div>
        </div>
      </div>
      <div class="row greybox">
        <div class="round">3</div>Hur vill du betala?
      </div>
      <div class="row whitebox">
        <div class="col">
          <input type="text" v-model="creditcard" placeholder="Kreditkortsnummer" />
        </div>
      </div>
      <div class="row whitebox">
        <div class="col">
          <input type="text" v-model="mm" placeholder="MM/ÅÅ" />
        </div>
        <div class="col">
          <input type="text" v-model="cvc" placeholder="CVC" />
        </div>
        <div class="col-2 verified-button" v-on:click="pwund()">tanka</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data: function() {
    return {
      phonenumber: "0729450596",
      selectedopt: 1,
      creditcard: "",
      mm: "",
      cvc: ""
    };
  },
  methods: {
    pwund: function() {
      alert(
        "You got pwned! Your moneys is mine! (read with russian accent). Muahahah!"
      );
    }
  }
};
</script>

<style scoped>
.amount {
  border-radius: 5px;
  border: #ebe4da solid 2px;
  padding: 20px;
}
.amount.selected {
  border-radius: 5px;
  border: #e2007a solid 2px;
  padding: 20px;
}
.verified-button {
  color: #fff;
  background-color: #e2007a;
  padding: 7px 18px;
  line-height: 40px;
  transition: background-color ease-in-out 0.15s, border-color ease-in-out 0.15s,
    color ease-in-out 0.15s;
  font-weight: bold;
  text-transform: uppercase;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  white-space: nowrap;
  font-size: 16px;
  border-radius: 3px;
  text-decoration: none;
}
input {
  outline: none;
  padding: 10px;
  font-size: 20px;
  padding-left: 15px;
  width: 100%;
}
.whitebox {
  padding: 15px;
}
.round {
  position: absolute;
  top: 15px;
  left: 15px;
  height: 35px;
  width: 35px;
  line-height: 35px;
  text-align: center;
  font-size: 20px;
  text-align: center;
  background: #ffffff;
  border-radius: 20px;
}
.greybox {
  background: #efefef;
  padding: 15px;
  font-size: 20px;
  position: relative;
  padding-left: 60px;
}
.button-top:hover {
  border: 2px solid #111;
}
.button-top {
  display: inline-block;
  color: #fff;
  background-color: #e2007a;
  border: 2px solid #a9005b;
  padding: 7px 18px;
  line-height: 24px;
  transition: background-color ease-in-out 0.15s, border-color ease-in-out 0.15s,
    color ease-in-out 0.15s;
  font-weight: bold;
  text-transform: uppercase;
  text-align: center;
  vertical-align: middle;
  touch-action: manipulation;
  cursor: pointer;
  background-image: none;
  white-space: nowrap;
  font-size: 16px;
  border-radius: 3px;
  text-decoration: none;
}
.button-top:hover {
}
.icons {
  padding-top: 8px;
}
.logo-top {
  padding-top: 8px;
}
.top-link {
  line-height: 20px;
  font-size: 18px;
  padding-top: 12px;
  color: #111;
  text-transform: uppercase;
  cursor: pointer;
}
.top-link:hover {
  text-decoration: underline;
}
.top {
  background: #d8cab7;
  padding-top: 10px;
  padding-bottom: 10px;
}
.top2 {
  background: #ebe4da;
  padding-top: 20px;
  text-align: center;
  font-weight: bold;
  font-size: 28px;
  padding-bottom: 20px;
}
</style>