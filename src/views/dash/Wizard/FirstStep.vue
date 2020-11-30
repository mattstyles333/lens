<template>
  <div class="wrapper">

    <div class="section">
      <div class="container">
        <div class="main">
                                <md-progress-bar
            class="md-primary"
            :md-value="amount"
          />
          <div class="md-layout">

            <div class="md-layout-item md-size-50 md-small-size-100">
              <ProductZoomer
                :base-images="images"
                :base-zoomer-options="zoomerOptions"
              />
            </div>
            <div class="md-layout-item md-size-50 md-small-size-100">
              
              <h2 class="title">
                Lens Configurator
              </h2>
              <h3 class="main-price">
                $35
              </h3>
              
              <div class="md-layout pick-size">
              
                <div class="md-layout-item md-size-50 md-small-size-100">
                  <label>Select Lens Type</label>
                  <md-field>
                    <md-select
                      id="selectType"
                      v-model="selectType"
                      name="selectType"
                    >
                      <md-option value="distance">
                        Distance
                      </md-option>
                      <md-option value="reading">
                        Reading
                      </md-option>
                      <md-option value="varifocal">
                        Varifocal/Progressive
                      </md-option>
                    </md-select>
                  </md-field>
                </div>
                <div class="md-layout-item md-size-50 md-small-size-100">
                  <label>Select Lens Thickness</label>
                  <md-field>
                    <md-select
                      id="selectThickness"
                      v-model="selectThickness"
                      name="selectThickness"
                    >
                      <md-option value="standard">
                        1.5 Standard
                      </md-option>
                      <md-option value="thin">
                        1.6 Thin
                      </md-option>
                      <md-option value="thinner">
                        1.67 Thinner
                      </md-option>
                        <md-option value="thinnest">
                        1.74 Thinnest
                      </md-option>
                    </md-select>
                  </md-field>
                </div>
                <div class="md-layout-item md-size-50 md-small-size-100">
                  <label>Select Lens Coatings</label>
                  <md-field>
                    <md-select
                      id="selectCoatings"
                      v-model="selectThickness"
                      name="selectCoatings"
                    >
                      <md-option value="as">
                        Anti-Scratch
                      </md-option>
                      <md-option value="uv">
                        UV Coating
                      </md-option>
                      <md-option value="ar">
                        Anti-Reflective
                      </md-option>
                        <md-option value="blue-light">
                        Blue Light Filter
                      </md-option>
                    </md-select>
                  </md-field>
                </div>
                
          <div class="md-layout-item md-size-100">
          <md-button
            class="md-success md-just-icon md-round"
          >
            <md-icon></md-icon>
          </md-button>
                    <md-button
            class="md-warning md-just-icon md-round button-select"
          >
            <md-icon></md-icon>
          </md-button>
                    <md-button
            class="md-danger md-just-icon md-round"
          >
            <md-icon></md-icon>
          </md-button>
          <md-button
            class="md-default md-just-icon md-round"
          >
            <md-icon></md-icon>
          </md-button>
          </div>
          <div class="md-layout-item md-size-100">
          <md-checkbox v-model="checkbox1">
              Polarized
            </md-checkbox>
            <md-switch v-model="switch1">
              Toogle is on
            </md-switch>
                        <md-radio
              v-model="radio1"
              :value="true"
            >
              Radio is on
            </md-radio>
            <md-radio
              v-model="radio1"
              :value="false"
            >
                          Radio is off
            </md-radio>
          </div>
              </div>
              <div class="text-right">
                <md-button
                  class="md-rose md-round"
                >
                  Add To Cart <md-icon>shopping_cart</md-icon>
                </md-button>
              </div>
            </div>
          </div>
        </div>
        <div class="features text-center">
          <div class="md-layout">
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas
                icon-color="info"
                icon="local_shipping"
                text-center
              >
                <h4
                  slot="title"
                  class="info-title"
                >
                  2 Days Delivery
                </h4>
                <p slot="content">
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </info-areas>
            </div>
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas
                icon-color="success"
                icon="verified_user"
                text-center
              >
                <h4
                  slot="title"
                  class="info-title"
                >
                  Refundable Policy
                </h4>
                <p slot="content">
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </info-areas>
            </div>
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas
                icon-color="rose"
                icon="favorite"
                text-center
              >
                <h4
                  slot="title"
                  class="info-title"
                >
                  Popular Item
                </h4>
                <p slot="content">
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </info-areas>
            </div>
          </div>
        </div>
        
      </div>
    </div>
  </div>
</template>

<script>
import {InfoAreas } from "@/components";
import Mixins from "@/plugins/basicMixins";

export default {
  components: {
    InfoAreas,

  },
  mixins: [Mixins.HeaderImage],
  bodyClass: "product-page",
  data() {
    return {
      radio1: true,
      checkbox1: null,
      switch1: false,
      amount: 30,
      selectColor: "red",
      selectSize: "small",
      image: require("@/assets/img/examples/bg-product.jpg"),
      
      images: {
        normal_size: [
                   {
            id: 1,
            url: require("@/assets/img/lens/clear.webp")
          },
          {
            id: 2,
            url: require("@/assets/img/lens/sunglass-brown.webp")
          },
                             {
            id: 3,
            url: require("@/assets/img/lens/sunglass.webp")
          }
        ],
        large_size: [
                   {
            id: 1,
            url: require("@/assets/img/lens/clear.webp")
          },
          {
            id: 2,
            url: require("@/assets/img/lens/sunglass-brown.webp")
          },
                             {
            id: 3,
            url: require("@/assets/img/lens/sunglass.webp")
          }
        ],
      },
      zoomerOptions: {
        pane: "container-round",
        hoverDelay: 300,
        namespace: "inline-container",
        move_by_click: true,
        scroll_items: 4
      }
    };
  }
};
</script>
<style lang="scss">
.inline-container-zoomer-box {
  .preview-box {
    text-align: center;
    margin-bottom: 5vh;
    margin-top: 2vh;

    img {
      max-width: 60%;
    }
  }

  .control-box {
    margin-bottom: 30px;
  }

  .thumb-list img {
    padding: 18px 8px;
    border: 1px solid transparent;
    opacity: 0.8;
    transition: all 0.15s ease;

    &:hover {
      opacity: 1;
      border-color: #ddd;
    }
  }

  .responsive-image {
    max-width: 80%;
    border-radius: 3px;

    &.choosed-thumb {
      box-shadow: none !important;
      border-color: #ddd;
    }
  }

  .control {
    font-size: 14px;

    path {
      fill: #9fa4ab;
    }
  }
}
.button-select {
  border: solid !important;
}
</style>
