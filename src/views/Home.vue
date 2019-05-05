<template>
  <div class="home">
    <Overview />
    <Testpaket />
    <WieFunktioniert />
    <GetTestpaket />
  </div>
</template>

<script>
// @ is an alias to /src

import Overview from "@/components/Overview.vue";
import Testpaket from "@/components/Testpaket.vue";
import WieFunktioniert from "@/components/WieFunktioniert.vue";
import GetTestpaket from "@/components/GetTestpaket.vue";
export default {
  name: "home",
  components: {
    Overview,
    Testpaket,
    WieFunktioniert,
    GetTestpaket
  }
};
</script>
<style lang="scss">
a {
  text-decoration: none;
}
.btn {
  padding: 12px 20px;
  background: #00afab;
  color: #fff;
}
</style>
