<template>
  <div id="donate-container">
    <h2>Please Donate Here!</h2>
    <div class="paypal-donations">
      <a href="https://www.paypal.me/risinguptogether">
        <div class="btn">PAYPAL</div>
      </a>
    </div>
    <div class="venmo-donations">
      <a href="https://venmo.com/code?user_id=2770021717639168138">
        <div class="btn">VENMO</div>
      </a>
      <img class="venmo-qr" src="../assets/venmo-qr.png" />
    </div>
    <h2>Thank you for your lifesaving donations!</h2>
  </div>
</template>

<script>
export default {
  name: 'Donate',
  props: {
    url: String,
    height: Number
  }
}
</script>

<style scoped>
  h2 {
    margin: 0;
  }
  #donate-container {
    padding: 20px;
    box-shadow: 0px 4px 8px -2px rgba(128,128,128,1);
  }
  .venmo-donations {
    border-top: 1px solid #808080;
  }
  a {
    text-decoration: none;
  }
  .btn {
    background-color: #808080;
    color: white;
    padding: 10px 15px;
    margin: 10px;
    font-weight: 600;
  }
  .btn:hover {
    background-color: #bcbcbc;
    cursor: pointer;
    color: #2c3e50;
  }
  img.venmo-qr {
    width: 100px;
  }
</style>
