<template>
  <section>
    <h2>Wie es funktioniert</h2>
    <div class="row">
      <div class="col-left">
        <img src="../assets/images/lillydoo-your-trialbox-icon.svg" alt />
        <h3>DEIN TESTPAKET</h3>
        <p>
          Wir schenken Dir die Produkte,
          <br />Du übernimmst nur das Porto.
        </p>
      </div>
      <div class="col-center">
        <img src="../assets/images/lillydoo-your-subscription-icon.svg" alt />
        <h3>DEINE FLEXIBILITÄT</h3>
        <p>
          Erste Monatsbox nach 14 Tagen für 49,50 € erhalten.
          <br />Oder noch vor der ersten Lieferung kündigen
        </p>
        <a href="#">
          Erfahre hier mehr über das
          <br />LILLYDOO Windel-Abo.
        </a>
      </div>
      <div class="col-right">
        <img src="../assets/images/lillydoo-your-flexibility-icon.svg" alt />
        <h3>DEINE MONATSBOX</h3>
        <p>
          Jederzeit Designs oder Lieferintervalle anpassen oder die Windelgröße
          ändern.
        </p>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "WieFunktioniert"
};
</script>
<style lang="scss" scoped>
$breakpoint-xs: 575.98px;
$breakpoint-sm: 767.98px;
$breakpoint-md: 991.98px;
$breakpoint-l: 1024px;
$breakpoint-xl: 1199.98px;

section {
  background: #f8f8f8;
  text-align: center;
  color: #000;

  h2 {
    display: block;
    width: 100%;
    padding-bottom: 20px;
  }

  .row {
    align-items: flex-start;

    .col-left {
      width: 33.33%;
      padding: 0 20px;
    }
    .col-center {
      width: 33.33%;
      padding: 0 20px;

      a {
        display: block;
        margin: 30px auto;
        color: #00afab;
      }
    }
    .col-right {
      width: 33.33%;
      padding: 0 20px;
    }
    p {
      margin: 10px auto;
    }
  }
  @media (max-width: $breakpoint-xl) {
  }
  @media (max-width: $breakpoint-l) {
  }
  @media (max-width: $breakpoint-md) {
  }
  @media (max-width: $breakpoint-sm) {
    .row {
      flex-wrap: wrap;

      .col-left {
        width: 100%;
        margin-bottom: 25px;
      }
      .col-center {
        width: 100%;
        margin-bottom: 25px;
      }
      .col-right {
        width: 100%;
        margin-bottom: 25px;
      }
      p {
        margin: 10px auto;
      }
    }
  }
  @media (max-width: $breakpoint-xs) {
    .row {
      flex-wrap: wrap;

      .col-left {
        width: 100%;
        margin-bottom: 25px;
      }
      .col-center {
        width: 100%;
        margin-bottom: 25px;
      }
      .col-right {
        width: 100%;
        margin-bottom: 25px;
      }
      p {
        margin: 10px auto;
      }
    }
  }
}
</style>
