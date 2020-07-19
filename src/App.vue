<template>
  <div id="app">
    <div class="app-container">
      <HeaderComponent />
      <AboutComponent/>
      <ApplyComponent />
      <FaqComponent />
      <ClientComponent />
      <FooterComponent />
    </div>
  </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent'
import AboutComponent from './components/AboutComponent'
import ApplyComponent from './components/ApplyComponent'
import FaqComponent from './components/FaqComponent'
import FooterComponent from './components/FooterComponent'
import ClientComponent from './components/ClientComponent'

export default {
  name: 'App',
  components: {
    AboutComponent,
    ApplyComponent,
    FaqComponent,
    FooterComponent,
    HeaderComponent,
    ClientComponent,
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=Rubik:wght@300;400;500&display=swap');
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}

img {
  display: block;
  max-width: 100%;
}

a {
  text-decoration: none;
  letter-spacing: 0.05em;
  font-weight: 500;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

ul {
  list-style: none;
}

body {
  background-color: #FEF8F5;
  font-family: 'Rubik', sans-serif;
  font-size: 16px;
}

.app-container {
  max-width: 1600px;
  width: 100%;
  margin: 0 auto;
}
</style>
