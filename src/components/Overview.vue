<template>
  <section>
    <img src="../assets/images/oekotex_de.png" alt />
    <div class="row">
      <div class="col-left">
        <h1>
          Entdecke unsere
          <br />Hautfreundlichkeit
        </h1>
        <a class="btn" href="#">Jetzt Deine Größe wählen</a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Overview"
};
</script>
<style lang="scss" scoped>
$breakpoint-xs: 575.98px;
$breakpoint-sm: 767.98px;
$breakpoint-md: 991.98px;
$breakpoint-l: 1024px;
$breakpoint-xl: 1199.98px;

section {
  background: url("../assets/images/lillydoo-testpaket-header-large.jpg")
    no-repeat;
  background-position: center;
  background-size: cover;
  text-align: center;

  img {
    position: absolute;
    top: 10%;
    right: 10%;
    bottom: 0;
    max-width: 150px;
  }

  .row {
    .col-left {
      width: 50%;
    }
  }
  .btn {
    display: inline-block;
    margin-top: 35px;
    padding: 10px 15px;
    background: #00afab;
    font-family: cera_regular;
    font-size: 1.1rem;
    text-transform: uppercase;
    color: #fff;
  }
  @media (max-width: $breakpoint-xl) {
    img {
      top: 10%;
      right: 0;
    }
  }
  @media (max-width: $breakpoint-md) {
    min-height: 600px;
    align-items: flex-start;
    background: url("../assets/images/lillydoo-testpaket-header-small.jpg")
      no-repeat;
    background-position: center 85%;
    background-size: cover;

    img {
      top: 50%;
      right: 0;
    }
    .row {
      width: 100%;
      padding: 6vw 2vw;

      .col-left {
        width: 100%;
      }
    }
  }
  @media (max-width: $breakpoint-sm) {
    img {
      max-width: 100px;
      top: unset;
      right: 5%;
      bottom: 32%;
    }
    .row {
      padding-top: 15vh;
      padding-bottom: 30px;

      .col-left {
        width: 100%;
      }
    }
  }
  @media (max-width: $breakpoint-xs) {
    h1 {
      font-size: 2rem;
    }
  }
}
</style>
