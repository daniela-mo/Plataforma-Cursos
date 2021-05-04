<template>
  <div id="app">
    <Header />
    <router-view />
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header";
import Footer from "@/components/Footer";

export default {
  components: {
    Header,
    Footer,
  },
};
</script>

<style lang="scss">
:root {
  --color-background: #141313;
  --color-blecaute: #191820;
  --color-white: #fff;
  --color-light-silver: #bcbcbc;
  --color-light-blue: #00c0cd;
  --color-blue: #32b0fc;
  --color-lilac: #a398ff;
  --color-pink: #ff6a9d;
  --color-dark: #2c2b43;
  --color-black: #000;
  --color-gray-10: #f0f2f8;
  --color-gray-20: #d9dce6;
  --color-gray-50: #787887;
  --color-gray-80: #525166;
  --color-button: #fcc419;
}
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
body {
  font-family: "Inter", sans-serif;
}
html {
  scroll-behavior: smooth;
}
input,
button,
textarea,
fieldset,
legend,
label,
span {
  font-size: 1.4rem;
  outline: none;
}
li {
  font-size: 16px;
  line-height: 22px;
  color: var(--color-dark);
}
.overflow-hidden {
  overflow: hidden;
}
.container {
  width: 100%;
  margin: 0 auto;
  background: var(--color-blecaute);
}
</style>
