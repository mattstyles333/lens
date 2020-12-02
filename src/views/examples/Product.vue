<template>
  <div class="wrapper">
    <parallax
      class="page-header header-filter header-small"
      parallax-active="true"
      filter-color="grey"
      :style="headerStyle"
    >
      <div class="container">
        <div class="md-layout title-row">
          <div
            class="md-layout-item md-size-33 md-small-size-100 ml-auto text-right"
          ></div>
        </div>
      </div>
    </parallax>
    <div class="section">
      <div class="container">
        <div class="main main-raised">
          <div class="md-layout">
            <div class="md-layout-item md-size-100 md-medium-size-100">
              <div class="title text-center">
                <h1>Lens Configurator</h1>
              </div>
              <md-progress-bar class="md-primary" :md-value="amount" />
              <tabs
                :tab-active="1"
                :tab-name="[
                  'Frame Type',
                  'Usage',
                  'Lens',
                  'Color',
                  'Prescription',
                  'Shipping',
                ]"
                plain
                color-button="rose"
                ref="tabs"
              >
                <!-- here you can add your content for tab-content -->
                <template slot="tab-pane-1" >
                  <div class="md-layout">
                    <div
                      class="md-layout-item md-size-33 md-small-size-100 md-large-size-33"
                    >
                      <pricing-card card-plain>
                        <template slot="cardContent">
                          <h6 class="card-category text-gray">Full Rimmed</h6>
                          <div class="icon">
                            <i class="material-icons">weekend</i>
                          </div>
                          <h3 class="card-title">Free</h3>
                          <p class="card-description">
                            This is good if your company size is between 2 and
                            10 Persons.
                          </p>
                          <md-button
                            href="javascript:void(0)"
                            class="md-white md-round"
                          >
                            Choose Plan
                          </md-button>
                        </template>
                      </pricing-card>
                    </div>
                    <div
                      class="md-layout-item md-size-33 md-small-size-100 md-large-size-33"
                    >
                      <pricing-card>
                        <template slot="cardContent">
                          <h6 class="card-category text-gray">Semi Rimless</h6>
                          <div class="icon icon-rose">
                            <i class="material-icons">people</i>
                          </div>
                          <h3 class="card-title">$29</h3>
                          <p class="card-description">
                            This is good if your company size is between 2 and
                            10 Persons.
                          </p>
                          <md-button
                            href="javascript:void(0)"
                            class="md-rose md-round"
                          >
                            Choose Plan
                          </md-button>
                        </template>
                      </pricing-card>
                    </div>
                    <div
                      class="md-layout-item md-size-33 md-small-size-100 md-large-size-33"
                    >
                      <pricing-card card-plain>
                        <template slot="cardContent">
                          <h6 class="card-category text-gray">
                            Rimless
                          </h6>
                          <div class="icon">
                            <i class="material-icons">business</i>
                          </div>
                          <h3 class="card-title">$69</h3>
                          <p class="card-description">
                            This is good if your company size is between 11 and
                            99 Persons.
                          </p>
                          <md-button
                            href="javascript:void(0)"
                            class="md-white md-round"
                          >
                            Choose Plan
                          </md-button>
                        </template>
                      </pricing-card>
                    </div>
                  </div>
                  <div class="text-right">
                    <md-button
                      class="md-success md-round md-lg"
                      @click="
                        incrementSlider();
                        $refs.tabs.switchPanel('Usage');
                      "
                    >
                      Next
                    </md-button>
                  </div>
                </template>
                <template slot="tab-pane-2">
                  <div class="md-layout">
                    <div class="md-layout-item md-size-20 md-small-size-100">
                      <blog-card
                        card-plain
                        :shadow-normal="false"
                        :no-colored-shadow="false"
                        :card-image="cardBlogPost.cardBlogPost1"
                      >
                        <template slot="cardContent">
                          <h6 class="card-category text-info">Standard</h6>
                          <h4 class="card-title">No Prescription</h4>
                          <p class="card-description">
                            Standard no prescription sunglass or clear glasses
                            lens
                          </p>
                        </template>
                      </blog-card>
                    </div>
                    <div class="md-layout-item md-size-20 md-small-size-100">
                      <blog-card
                        card-plain
                        :shadow-normal="false"
                        :no-colored-shadow="false"
                        :card-image="cardBlogPost2.cardBlogPost1"
                      >
                        <template slot="cardContent">
                          <h6 class="card-category text-info">Standard</h6>
                          <h4 class="card-title">Distance</h4>
                          <p class="card-description">
                            Like so many organizations these days, Autodesk is a
                            company in transition. It was until recently a
                            traditional boxed software company selling licenses.
                            <a href="javascript:void(0)"> Read More </a>
                          </p>
                        </template>
                      </blog-card>
                    </div>
                    <div class="md-layout-item md-size-20 md-small-size-100">
                      <blog-card
                        card-plain
                        :shadow-normal="false"
                        :no-colored-shadow="false"
                        :card-image="cardBlogPost2.cardBlogPost1"
                      >
                        <template slot="cardContent">
                          <h6 class="card-category text-info">Standard</h6>
                          <h4 class="card-title">Reading</h4>
                          <p class="card-description">
                            Like so many organizations these days, Autodesk is a
                            company in transition. It was until recently a
                            traditional boxed software company selling licenses.
                            <a href="javascript:void(0)"> Read More </a>
                          </p>
                        </template>
                      </blog-card>
                    </div>
                    <div class="md-layout-item md-size-20 md-small-size-100">
                      <blog-card
                        card-plain
                        :shadow-normal="false"
                        :no-colored-shadow="false"
                        :card-image="cardBlogPost2.cardBlogPost2"
                      >
                        <template slot="cardContent">
                          <h6 class="card-category text-danger">Advanced</h6>
                          <h4 class="card-title">Bifocals</h4>
                          <p class="card-description">
                            Like so many organizations these days, Autodesk is a
                            company in transition. It was until recently a
                            traditional boxed software company selling licenses.
                            <a href="javascript:void(0)"> Read More </a>
                          </p>
                        </template>
                      </blog-card>
                      Pick the best plan for you
                    </div>
                    <div class="md-layout-item md-size-20 md-small-size-100">
                      <blog-card
                        card-plain
                        :shadow-normal="false"
                        :no-colored-shadow="false"
                        :card-image="cardBlogPost2.cardBlogPost2"
                      >
                        <template slot="cardContent">
                          <h6 class="card-category text-danger">Advanced</h6>
                          <h4 class="card-title">Progressive / Varifocals</h4>
                          <p class="card-description">
                            Like so many organizations these days, Autodesk is a
                            company in transition. It was until recently a
                            traditional boxed software company selling licenses.
                            <a href="javascript:void(0)"> Read More </a>
                          </p>
                        </template>
                      </blog-card>
                    </div>
                  </div>
                  <div class="text-right">
                    <md-button
                      class="md-success md-round md-lg"
                      @click="
                        incrementSlider();
                        $refs.tabs.switchPanel('Lens');
                      "
                    >
                      Next
                    </md-button>
                  </div>
                </template>
                <template slot="tab-pane-3">
                  <div class="md-layout">
                    <div class="md-layout-item md-size-50 md-small-size-100">
                      <ProductZoomer
                        :base-images="lensImages"
                        :base-zoomer-options="zoomerOptions"
                      />
                    </div>
                    <div
                      class="md-layout-item md-size-50 md-small-size-100 text-left"
                    >
                      <br />

                      <div class="md-layout pick-size">
                        <div
                          class="md-layout-item md-size-50 md-small-size-100"
                        >
                          <label>Select Lens Thickness</label>
                          <md-field>
                            <md-select
                              id="selectThickness"
                              name="selectThickness"
                            >
                              <md-option value="standard">
                                1.5 Standard
                              </md-option>
                              <md-option value="thin"> 1.6 Thin </md-option>
                              <md-option value="thinner">
                                1.67 Thinner
                              </md-option>
                              <md-option value="thinnest">
                                1.74 Thinnest
                              </md-option>
                            </md-select>
                          </md-field>
                        </div>
                        <div
                          class="md-layout-item md-size-50 md-small-size-100"
                        >
                          <label>Select Lens Coatings</label>
                          <md-field>
                            <md-select
                              id="selectCoatings"
                              name="selectCoatings"
                            >
                              <md-option value="as"> Anti-Scratch </md-option>
                              <md-option value="uv"> UV Coating </md-option>
                              <md-option value="ar">
                                Anti-Reflective
                              </md-option>
                              <md-option value="blue-light">
                                Blue Light Filter
                              </md-option>
                            </md-select>
                          </md-field>
                        </div>
                      </div>
                      <div class="text-right">
                        <md-button
                          class="md-success md-round md-lg"
                          @click="
                            incrementSlider();
                            $refs.tabs.switchPanel('Color');
                          "
                        >
                          Next
                        </md-button>
                      </div>
                    </div>
                  </div>
                </template>
                <template slot="tab-pane-4">
                  <div class="md-layout">
                    <div class="md-layout-item md-size-50 md-small-size-100">
                      <ProductZoomer
                        :base-images="lensImages"
                        :base-zoomer-options="zoomerOptions"
                      />
                    </div>
                    <div
                      class="md-layout-item md-size-50 md-small-size-100 text-left"
                    >
                      <div class="md-layout">
                        <h3>Select Color</h3>
                        <div class="md-layout-item md-size-100">
                          <md-button class="md-success md-just-icon md-round">
                            <md-icon></md-icon>
                          </md-button>
                          <md-button
                            class="md-warning md-just-icon md-round button-select"
                          >
                            <md-icon></md-icon>
                          </md-button>
                          <md-button class="md-danger md-just-icon md-round">
                            <md-icon></md-icon>
                          </md-button>
                          <md-button class="md-default md-just-icon md-round">
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
                          <md-radio v-model="radio1" :value="true">
                            Radio is on
                          </md-radio>
                          <md-radio v-model="radio1" :value="false">
                            Radio is off
                          </md-radio>
                        </div>
                      </div>
                      <div class="text-right">
                        <md-button
                          class="md-success md-round md-lg"
                          @click="
                            incrementSlider();
                            $refs.tabs.switchPanel('Prescription');
                          "
                        >
                          Next
                        </md-button>
                      </div>
                    </div>
                  </div>
                </template>
                <template slot="tab-pane-5">
                  Completely synergize resource taxing relationships via premier
                  niche markets. Professionally cultivate one-to-one customer
                  service with robust ideas.
                  <br /><br />
                  Dynamically innovate resource-leveling customer service for
                  state of the art customer service.
                  <div class="text-right">
                    <md-button
                      class="md-success md-round md-lg"
                      @click="
                        incrementSlider();
                        $refs.tabs.switchPanel('Shipping');
                      "
                    >
                      Next
                    </md-button>
                  </div>
                </template>
                <template slot="tab-pane-6">
                  Completely synergize resource taxing relationships via premier
                  niche markets. Professionally cultivate one-to-one customer
                  service with robust ideas.
                  <br /><br />
                  Dynamically innovate resource-leveling customer service for
                  state of the art customer service.
                  <div class="text-right">
                    <md-button
                      class="md-success md-round md-lg"
                      @click="incrementSlider"
                    >
                      Next
                    </md-button>
                  </div>
                </template>
              </tabs>
            </div>
          </div>
        </div>
        <div class="features text-center">
          <div class="md-layout">
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas icon-color="info" icon="local_shipping" text-center>
                <h4 slot="title" class="info-title">2 Days Delivery</h4>
                <p slot="content">
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </info-areas>
            </div>
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas icon-color="success" icon="verified_user" text-center>
                <h4 slot="title" class="info-title">Refundable Policy</h4>
                <p slot="content">
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </info-areas>
            </div>
            <div class="md-layout-item md-size-33 md-small-size-100">
              <info-areas icon-color="rose" icon="favorite" text-center>
                <h4 slot="title" class="info-title">Popular Item</h4>
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
import Mixins from "@/plugins/basicMixins";

import {
  BlogCard,
  FullBgCard,
  PricingCard,
  Tabs,
  InfoAreas,
} from "@/components";

export default {
  components: {
    InfoAreas,
    Tabs,
    BlogCard,
    PricingCard,
  },
  mixins: [Mixins.HeaderImage],
  bodyClass: "product-page",

  data() {
    return {
      cardBlogPost: {
        cardBlogPost1: require("@/assets/img/examples/card-blog4.jpg"),
        cardBlogPost2: require("@/assets/img/office2.jpg"),
      },
      cardBlogPost2: {
        cardBlogPost1: require("@/assets/img/examples/blog5.jpg"),
        cardBlogPost2: require("@/assets/img/examples/blog7.jpg"),
      },
      cardBlogPost3: {
        cardBlogPost1: require("@/assets/img/examples/blog8.jpg"),
      },

      radio1: true,
      checkbox1: null,
      switch1: false,
      amount: 100 / 6,
      selectColor: "red",
      selectSize: "small",
      image: require("@/assets/img/lens/background2.jpeg"),

      lensImages: {
        normal_size: [
          {
            id: 1,
            url: require("@/assets/img/lens/clear.webp"),
          },
          {
            id: 2,
            url: require("@/assets/img/lens/sunglass-brown.webp"),
          },
          {
            id: 3,
            url: require("@/assets/img/lens/sunglass.webp"),
          },
        ],
        large_size: [
          {
            id: 1,
            url: require("@/assets/img/lens/clear.webp"),
          },
          {
            id: 2,
            url: require("@/assets/img/lens/sunglass-brown.webp"),
          },
          {
            id: 3,
            url: require("@/assets/img/lens/sunglass.webp"),
          },
        ],
      },
      zoomerOptions: {
        pane: "container-round",
        hoverDelay: 300,
        namespace: "inline-container",
        move_by_click: true,
        scroll_items: 4,
      },
    };
  },
  methods: {
    incrementSlider: function () {
      this.amount += 100 / 6;
    },
  },
};
</script>
<style lang="scss">
.disabledTab{
      pointer-events: none;
  }
.nav-tabs {
  justify-content: center !important;
}
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
