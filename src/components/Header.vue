<script setup>

</script>

<template>
  <div class="test"></div>
  <header>
    <div class="logo">
      <img alt="Vue logo" class="logo" src="/logoPanda.png"/>
    </div>
    <div class="title">
      <h1>Nicolas Signori</h1>
      <span>Woofi7</span>
    </div>
    <div class="right">
      <div class="language">
        <a href="https://nsignori.ca" hreflang="fr">FR</a> / <a href="https://nsignori.ca/en" hreflang="en">EN</a>
      </div>
      <div class="links">
        <a href="mailto:n.signo@hotmail.com">n.signo@hotmail.com <font-awesome-icon icon="fa-solid fa-envelope" /></a>
        <a href="https://github.com/woofi7">Github/woofi7 <font-awesome-icon icon="fa-brands fa-github" /></a>
        <a href="https://www.linkedin.com/in/nicolas-signori/">LinkedIn/nicolas-signori <font-awesome-icon icon="fa-brands fa-linkedin" /></a>
      </div>
    </div>

  </header>
</template>

<style scoped>
header {
  position: sticky;
  top: 0;
  left: 0;
  margin: -2rem -2rem 0 -2rem;
  background-color: #101010;
  padding: 0.5rem;
  flex-wrap: wrap;

  z-index: 2;
  display: flex;
  justify-content: space-between;
  align-items: center;
  gap: 0.5rem;
}

@media screen and (max-width: 600px) {
  .test {
    height: 170px;
  }
  header {
    position: absolute;
    margin: 0;
    justify-content: center;
  }
  .right {
    width: 100%;
    justify-content: space-between !important;
    padding-left: 1rem;
    padding-right: 1rem;
  }
}

.title {
  display: flex;
  flex-direction: column;
  align-items: flex-end;

  & > h1 {
    color: white;
  }
  & > span {
    margin-top: -0.5em;
    color: darkred;
  }
}

.logo {
  height: 80px;
}

.right {
  display: flex;
  align-items: center;
  justify-content: flex-end;
  flex-wrap: wrap-reverse;
  gap: 2rem;
  & > .language a {
    color: white;
  }

  & > .links {
     display: flex;
     flex-direction: column;
     align-items: flex-end;
     gap: 0.2em;
   }
}


</style>