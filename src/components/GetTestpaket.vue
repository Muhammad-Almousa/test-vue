<template>
  <section>
    <h2>Dein Testpaket enthält</h2>
    <div class="row">
      <div class="col-left">
        <div class="img-wrapper">
          <img
            src="../assets/images/lillydoo-little-blowballs-design-preview-tp.jpg"
            alt
          />
        </div>
        <div class="text-wrapper">
          <h3>10 LILLYDOO WINDELN</h3>
          <ul>
            <li>0 % Parfüme & Lotionen, 100 % LILLYDOO Schutz</li>
            <li>Extra weich und mit idealer Passform</li>
          </ul>
        </div>
      </div>
      <div class="col-right">
        <div class="img-wrapper">
          <img src="../assets/images/sensitive-wipes-15-small.jpg" alt />
        </div>
        <div class="text-wrapper">
          <h3>15 FEUCHTTÜCHER MIT 99 % WASSER</h3>
          <ul>
            <li>0 % Parfüme & PEGs, 100 % biologisch abbauba</li>
            <li>Natürlich rein, extra mild, Alternative zu "Wasser & Watte</li>
          </ul>
        </div>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "GetTestpaket"
};
</script>
<style lang="scss" scoped>
$breakpoint-md: 767.98px;
$breakpoint-xs: 575.98px;
section {
  h2 {
    width: 100%;
    text-align: center;
  }
  .row {
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: flex-start;

    .col-left {
      display: flex;
      flex-flow: row nowrap;
      align-items: flex-start;
      width: 50%;

      .img-wrapper {
        width: 25%;

        img {
          max-width: 100%;
        }
        @media (max-width: $breakpoint-xs) {
          width: 50%;
        }
      }

      .text-wrapper {
        text-align: left;

        h3 {
          margin-top: 0;
        }

        ul {
          padding-left: 16px;
        }
      }
      @media (max-width: $breakpoint-md) {
        width: 100%;
        margin-bottom: 30px;
      }
    }

    .col-right {
      display: flex;
      flex-flow: row nowrap;
      align-items: flex-start;
      width: 45%;

      h3 {
        margin-top: 0;
      }

      .img-wrapper {
        width: 25%;
        margin-right: 20px;

        img {
          max-width: 100%;
        }

        @media (max-width: $breakpoint-xs) {
          width: 50%;
        }
      }

      .text-wrapper {
        text-align: left;

        ul {
          padding-left: 16px;
        }
      }
      @media (max-width: $breakpoint-md) {
        width: 100%;
      }
    }
  }
}
</style>
