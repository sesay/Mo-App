<template>
  <div class="footer-wrapper">
    <div class="footer-container img-bg">
      <div class="footer-group components">
        <QuoteComponent :text="quote" />
        <FormComponent />
      </div>
      <NavigationComponent :nav="nav" />
    </div>
    <div class="footer-container">
      <div class="copyright-info footer-group">
      <p>Copyright @ 2019</p>
      <div class="social-links">
        <ul>
          <li> 
            <a href="#">
              <span class="icon facebook"></span>
            </a>
          </li>
          <li> 
            <a href="#">
              <span class="icon twitter"></span>
            </a>
          </li>
          <li> 
            <a href="#">
              <span class="icon instagram"></span>
            </a>
          </li>
        </ul>
      </div>
    </div>
    </div>
  </div>
</template>

<script>
import QuoteComponent from './SharedComponent/QuoteComponent'
import NavigationComponent from './NavigationComponent'
import FormComponent from './SharedComponent/FormComponent'


import data from './../model/data';

export default {
  components: {
    FormComponent,
    QuoteComponent,
    NavigationComponent,
  },
  data: function() {
    return {
      quote: data.footer.quote,
      nav: data.footer.navigation
    }
  },
  methods: {

  }
}
</script>

<style>
  .footer-wrapper {
    margin-top: 104px;
  }

  .footer-group.components {
    display: flex;
    flex-flow: row;
    align-items: flex-start;
    padding-top: 60px;
    margin-bottom: 180px;
  }

  .footer-group {
    margin-left: auto;
    margin-right: 135px;
    max-width: 1025px;
    width: 100%;
  }

  .footer-container .navigation-component .logo {
    width: 170px;
  }

  .contact-form {
    flex: 0 0 550px;
    margin-left: auto;
  }

  .footer-container {
    max-width: 1400px;
    width: 100%;
  }

  .footer-container.img-bg {
    padding-bottom: 98px;
    background: url('./../assets/footer-bg.png') no-repeat;
    background-size: cover;
    position: relative;
  }

  .footer-container .navigation-component {
    max-width: 1025px;
    width: 100%;
    margin-left: auto;
    margin-right: 135px;
  }

  .footer-container .navigation a {
    font-weight: 400;
    font-size: 16px;
  }

  .footer-container .contact-form {
    flex: 0 0 550px;
    margin-left: auto;
  }

  .footer-container .quote {
    padding-left: 40px;
    color: #fff;
    margin-top: 210px;
    font-size: 20px;
    line-height: 30px;
  }

  .copyright-info {
    max-width: 1025px;
    width: 100%;
    justify-content: space-between;
    height: 180px;
    font-weight: 300;
    display: flex;
    align-items: center;
    background: #FEF8F5;
  }

  .social-links li {
    display: inline-block;
  }

  .social-links li:not(:last-child) a {
    margin-right: 30px;
  }

  .social-links a span {
    display: inline-block;
    background-size: contain !important;
    width: 36px;
    height: 36px;
  }

  .container {
    max-width: 1400px;
    width: 100%;
  }

  .social-links a span.facebook {
    background: url('./../assets/icon-facebook.png') no-repeat;
  }
  .social-links a span.twitter {
    background: url('./../assets/icon-twitter.png') no-repeat;
  }
  .social-links a span.instagram {
    background: url('./../assets/icon-instagram.png') no-repeat;
  }
</style>