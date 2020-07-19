<template>
  <div class="contact-form">
    <form action="#">
      <div class="input-field">
        <label for="name">Name</label>
        <input type="text" name="name" />
      </div>
      <div class="input-field">
        <label for="name">Email Address</label>
        <input type="email" name="email" value="Your email adress" />
      </div>
      <button type="submit">
        get started <i class="arrow"></i>
      </button>
    </form>
  </div>
</template>

<script>
export default {
  components: {
  },
  data: function() {
    return {
    }
  },
  methods: {

  }
}
</script>

<style>
  .contact-form {
    width: 550px;
    background: #FFFFFF;
    box-shadow: 0px 20px 40px rgba(238, 77, 71, 0.1);
    border-radius: 10px;
    padding: 50px 75px;
  }

  .contact-form input {
    background: #FFFFFF;
    border: 1px solid rgba(238, 77, 71, 0.5);
    box-sizing: border-box;
    border-radius: 5px;
    height: 60px;
    width: 100%;
    padding: 25px 0 25px 40px;
    font-size: 18px;
    outline: none;
  }

  .contact-form input:focus {
    border: 2px solid #EE4D47;
    box-shadow: 0px 20px 40px rgba(238, 77, 71, 0.2);
    font-weight: bold;
  }

  .contact-form .input-field label {
    font-weight: 300;
    font-size: 16px;
    line-height: 40px;
    margin-bottom: 5px;
    display: block;
  }

  .input-field:nth-child(2) {
    margin-top: 30px;
  }

  button[type="submit"] {
    background: #EE4D47;
    border-radius: 5px;
    display: inline-block;
    min-width: 220px;
    height: 60px;
    color: #fff;
    font-weight: bold;
    font-size: 16px;
    line-height: 19px;
    text-transform: uppercase;
    border: 0;
     margin-top: 30px;
  }

  button[type="submit"] > i {
    background: url('./../../assets/arrow.png') no-repeat;
    background-size: contain;
    display: inline-block;
    width: 30px;
    height: 12px;
    margin-left: 20px;
  }
</style>