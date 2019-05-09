<template>
  <section>
    <div class="row">
      <img class="top-left" src="../assets/images/oekotex_de.png" alt />
      <div class="col-left">
        <img
          v-for="(item, index) in packets"
          :class="{ 'img-active': activeIndex === index }"
          :key="item.id"
          :src="require('../assets/images/' + item.image)"
          alt
        />
      </div>
      <div class="col-right">
        <h2>Unser gratis Testpaket</h2>
        <h3>Wähle Deine Grösse</h3>
        <ul class="choose-list">
          <li
            class="list-item"
            v-for="(packet, index) in packets"
            :class="{ active: activeIndex === index }"
            :key="packet.id"
            @click="setActive(index)"
          >
            {{ packet.size }}
            <br />
            {{ packet.weight }}
          </li>
        </ul>
        <p>
          Teste jetzt unsere Windeln und Feuchttücher - In Größe 1 - 3 enthält
          unser Testpaket unsere Feuchttücher mit 99 % Wasser, ab Gr. 4 erhältst
          Du unsere Sensitiven Feuchttücher. Wir zahlen die Produkte, Du nur den
          Versand.
        </p>
        <ul class="list">
          <li>
            Automatischer Übergang ins jederzeit kündbare Windel-Abo für 49,50 €
            pro Lieferung.
          </li>
          <li>
            Preise inkl. MwSt., ggf. zzgl.
            <a href="https://www.lillydoo.com/de/zahlung-und-versand"
              >Versandkosten</a
            >
          </li>
        </ul>
        <a href="#" class="btn">In den Warenkorb legen</a>
      </div>
    </div>
  </section>
</template>
<script>
export default {
  name: "Testpaket",
  props: ["packet"],
  methods: {
    setActive(index) {
      this.activeIndex = index;
    }
  },
  data() {
    return {
      packets: [
        {
          id: 1,
          size: 1,
          weight: "(2-3 KG)",
          image: "lillydoo-testpaket-10.jpg"
        },
        {
          id: 2,
          size: 2,
          weight: "(2-3 KG)",
          image: "lillydoo-testpaket-20.jpg"
        },
        {
          id: 3,
          size: 3,
          weight: "(2-3 KG)",
          image: "lillydoo-testpaket-30.jpg"
        },
        {
          id: 4,
          size: 4,
          weight: "(2-3 KG)",
          image: "lillydoo-testpaket-40.jpg"
        },
        {
          id: 5,
          size: 5,
          weight: "(2-3 KG)",
          image: "lillydoo-testpaket-50.jpg"
        }
      ],
      activeIndex: 0
    };
  }
};
</script>
<style lang="scss" scoped>
$breakpoint-xs: 575.98px;
$breakpoint-sm: 767.98px;
$breakpoint-md: 991.98px;
$breakpoint-xl: 1199.98px;
section {
  padding: 0;

  .row {
    align-items: flex-start;
    justify-content: space-between;
    padding-bottom: 5vh;

    img.top-left {
      position: absolute;
      top: 15%;
      left: 0;
      max-width: 170px;
      z-index: 2;

      @media (min-width: $breakpoint-xl) {
        left: 5%;
      }
      @media (max-width: $breakpoint-md) {
        top: 8%;
        left: 5%;
        max-width: 120px;
      }
      @media (max-width: $breakpoint-sm) {
        top: 8%;
        left: 5%;
        max-width: 120px;
      }
      @media (max-width: $breakpoint-xs) {
        top: 8%;
        max-width: 100px;
      }
    }

    .col-left {
      width: 50%;

      img {
        max-width: 100%;
        display: none;
        opacity: 0;
        transition: all 5s;
      }
      .img-active {
        display: block;
        opacity: 1;
      }
    }

    .col-right {
      width: 40%;

      h2 {
        margin: 0px;
      }

      h3 {
        text-transform: uppercase;
      }

      .choose-list {
        display: flex;
        flex-flow: row wrap;
        margin-bottom: 30px;
        padding: 0;
        list-style: none;

        li {
          width: 25%;
          max-width: 100px;
          min-height: 60px;
          margin-right: 10px;
          margin-bottom: 10px;
          padding: 10px 0;
          border: 1px solid #7c7c7c;
          color: #7c7c7c;
          text-align: center;
          cursor: pointer;

          &.active {
            border: none;
            background: #00afab;
            color: #fff;
          }
          &:hover {
            border: none;
            background: #00afab;
            color: #fff;
          }
        }
        @media (min-width: $breakpoint-xl) {
          flex-wrap: nowrap;
        }
      }
      p {
        margin-bottom: 30px;
      }
      .list {
        margin-bottom: 20px;
        padding-left: 18px;

        li {
          &:first-child {
            color: #00afab;
          }

          a {
            color: #00afab;
          }
        }
      }
      .btn {
        display: inline-block;
        width: 100%;
        text-align: center;
        text-transform: uppercase;
      }
    }
  }
  @media (max-width: $breakpoint-md) {
    img.top-left {
      top: 0;
    }
    .row {
      width: 100%;
      padding-left: 4vw;
      padding-right: 4vw;
    }
  }
  @media (max-width: $breakpoint-sm) {
    .row {
      flex-wrap: wrap;
      .col-left {
        width: 100%;
        margin-bottom: 30px;
      }

      .col-right {
        width: 100%;

        .choose-list {
          flex-wrap: wrap;

          li {
            width: 25%;
          }
        }
      }
    }
  }
}
</style>
