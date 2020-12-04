<template>
  <div class="wrapper">
    <!-- Headers 3 -->
    <div class="section section-header-3 pt-0 pb-0">
      <el-carousel
        indicator-position="none"
        class="no-border no-height"
        trigger="click"
        :interval="5000"
      >
        <el-carousel-item>
          <div class="page-header header-filter" :style="header('3')">
            <div class="container">
              <div class="md-layout">
                <div
                  class="md-layout-item md-size-66 md-small-size-100 text-left"
                >
                  <h1 class="title">
                    There Will Be Blood-Red Trees
                  </h1>
                  <h4>
                    For weeks now, Romans have been breathlessly awaiting the
                    presentation of the Italian capital’s official Christmas
                    tree, a year after the resounding social media debacle that
                    felled last year’s fir.
                  </h4>
                  <br />
                  <div class="buttons">
                    <md-button
                      href="javascript:void(0)"
                      class="md-danger md-lg"
                    >
                      Read More
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-twitter md-simple md-white md-just-icon"
                    >
                      <i class="fab fa-twitter" />
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-facebook md-simple md-white md-just-icon"
                    >
                      <i class="fab fa-facebook-square" />
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-simple md-white md-just-icon"
                    >
                      <i class="fab fa-get-pocket" />
                    </md-button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="page-header header-filter" :style="header('4')">
            <div class="container">
              <div class="md-layout">
                <div
                  class="md-layout-item md-size-66 md-small-size-100 mx-auto text-center"
                >
                  <h1 class="title">
                    Material Kit PRO
                  </h1>
                  <h4>
                    While the wildfire, known as the Woolsey Fire, raged through
                    the slopes and canyons over the next two weeks, scorching
                    over 1,500 buildings and killing three people, park rangers
                    in the Santa Monica Mountains.
                  </h4>
                  <br />
                  <h6>Connect with us on:</h6>
                  <div class="buttons">
                    <md-button
                      href="javascript:void(0)"
                      class="md-twitter md-simple md-white md-lg md-just-icon ml-auto"
                    >
                      <i class="fab fa-twitter" />
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-facebook md-simple md-white md-lg md-just-icon"
                    >
                      <i class="fab fa-facebook-square" />
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-google md-simple md-white md-lg md-just-icon"
                    >
                      <i class="fab fa-google-plus-g" />
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-instagram md-simple md-white md-lg md-just-icon mr-auto"
                    >
                      <i class="fab fa-instagram" />
                    </md-button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </el-carousel-item>
        <el-carousel-item>
          <div class="page-header header-filter" :style="header('5')">
            <div class="container">
              <div class="md-layout">
                <div
                  class="md-layout-item md-size-66 md-small-size-100 ml-auto text-right"
                >
                  <h1 class="title">
                    Mountain Dew throwback bring real sugar back to sodas once
                    again
                  </h1>
                  <h4>
                    They’re baaaack! I just spotted the greatest beverages on
                    Earth in my local Rite Aid while shopping for New Year’s Eve
                    refreshments.
                  </h4>
                  <br />
                  <div class="buttons">
                    <md-button
                      href="javascript:void(0)"
                      class="md-white md-simple md-lg ml-auto"
                    >
                      <md-icon>share</md-icon> Share Offer
                    </md-button>
                    <md-button
                      href="javascript:void(0)"
                      class="md-danger md-lg"
                    >
                      <md-icon>shopping_cart</md-icon> Shop Now
                    </md-button>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </el-carousel-item>
      </el-carousel>
    </div>
    <!-- end Headers 3 -->
    <!-- Features 3 -->
    <div class="section section-features-3">
      <div class="container">
        <div class="md-layout">
          <div class="md-layout-item md-size-50 md-small-size-100">
            <div class="phone-container">
              <img :src="iphone" />
            </div>
          </div>
          <div class="md-layout-item md-size-50 md-small-size-100">
            <!-- Some <br /> tags to push the text to align with the image, you can remove it if you have more text on the right side :-) -->
            <h2 class="title">
              Your life will be much easier
            </h2>
            <info-areas info-horizontal icon-color="primary" icon="extension">
              <h4 slot="title" class="info-title">
                Hundreds of Components
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
            <info-areas
              info-horizontal
              icon-color="primary"
              icon="child_friendly"
            >
              <h4 slot="title" class="info-title">
                Ease to Use
              </h4>
              <div slot="content" class="description">
                <p>
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </div>
            </info-areas>
            <info-areas info-horizontal icon-color="primary" icon="watch_later">
              <h4 slot="title" class="info-title">
                Fast Prototyping
              </h4>
              <div slot="content" class="description">
                <p>
                  Divide details about your product or agency work into parts.
                  Write a few lines about each one. A paragraph describing a
                  feature will be enough.
                </p>
              </div>
            </info-areas>
          </div>
        </div>
      </div>
    </div>
    <!-- end Features 3 -->
    <!-- Features 5 -->
    <div class="section section-features-5" :style="features5">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-66 md-small-size-100 mx-auto text-center"
          >
            <h2 class="title">
              Your life will be much easier
            </h2>
          </div>
        </div>
      </div>

      <div class="container">
        <div class="md-layout">
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="code">
              <h4 slot="title" class="info-title">
                For Developers
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="format_paint">
              <h4 slot="title" class="info-title">
                For Designers
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="dashboard">
              <h4 slot="title" class="info-title">
                Bootstrap Grid
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
        </div>
        <div class="md-layout">
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="view_carousel">
              <h4 slot="title" class="info-title">
                Example Pages Included
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="access_time">
              <h4 slot="title" class="info-title">
                Save Time
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
          <div class="md-layout-item md-size-33 md-small-size-100">
            <info-areas text-center icon="attach_money">
              <h4 slot="title" class="info-title">
                Save Money
              </h4>
              <div slot="content" class="description">
                <p>
                  The moment you use Material Kit, you know you’ve never felt
                  anything like it. With a single use, this powerfull UI Kit
                  lets you do more than ever before.
                </p>
              </div>
            </info-areas>
          </div>
        </div>
      </div>
    </div>
    <!-- end Features 5 -->
    <!-- Projects 4 -->
    <div class="section section-projects-4">
      <div class="container">
        <div class="md-layout">
          <div
            class="md-layout-item md-size-66 md-small-size-100 justify-content-center mx-auto text-center"
          >
            <h2 class="title">
              Some of Our Awesome Products - 4
            </h2>
            <h5 class="description">
              This is the paragraph where you can write more details about your
              projects. Keep you user engaged by providing meaningful
              information.
            </h5>
          </div>
        </div>
        <div class="md-layout">
          <div class="md-layout-item md-size-40 md-small-size-100 ml-auto">
            <full-bg-card :card-image="cardProject3.cardProject2">
              <template slot="cardContent">
                <badge type="rose">
                  Client: Apple
                </badge>

                <a href="javascript:void(0)">
                  <h2 class="card-title">Beautiful Project</h2>
                </a>
                <p class="card-description">
                  Don't be scared of the truth because we need to restart the
                  human foundation in truth.
                </p>
              </template>
            </full-bg-card>
          </div>
          <div class="md-layout-item md-size-40 md-small-size-100 mr-auto">
            <info-areas info-horizontal icon-color="info" icon="format_paint">
              <h4 slot="title" class="info-title">
                Graphic Design
              </h4>
              <p slot="content">
                We've created the design of the website using modern
                Technologies like Sketch. It was a very interesting
                collaboration.
              </p>
            </info-areas>
            <info-areas info-horizontal icon-color="primary" icon="code">
              <h4 slot="title" class="info-title">
                Fully Coded in HTML5
              </h4>
              <p slot="content">
                We've developed the website with HTML5 and CSS3. The client has
                access to the code using GitHub.
              </p>
            </info-areas>
            <info-areas info-horizontal icon-color="danger" icon="dashboard">
              <h4 slot="title" class="info-title">
                CMS Admin Dashboard
              </h4>
              <p slot="content">
                There is also a Fully Customizable CMS Admin Dashboard for this
                product.
              </p>
            </info-areas>
          </div>
        </div>
        <hr />
        <div class="md-layout">
          <div class="md-layout-item md-size-40 md-small-size-100 ml-auto">
            <info-areas info-horizontal icon-color="rose" icon="timeline">
              <h4 slot="title" class="info-title">
                Marketing
              </h4>
              <p slot="content">
                We've created the marketing campaign of the website. It was a
                very interesting collaboration.
              </p>
            </info-areas>
            <info-areas info-horizontal icon-color="success" icon="code">
              <h4 slot="title" class="info-title">
                Fully Coded in HTML5
              </h4>
              <p slot="content">
                We've developed the website with HTML5 and CSS3. The client has
                access to the code using GitHub.
              </p>
            </info-areas>
            <info-areas info-horizontal icon-color="info" icon="group">
              <h4 slot="title" class="info-title">
                Build Audience
              </h4>
              <p slot="content">
                There is also a Fully Customizable CMS Admin Dashboard for this
                product.
              </p>
            </info-areas>
          </div>
          <div class="md-layout-item md-size-40 md-small-size-100 mr-auto">
            <full-bg-card :card-image="cardProject4.cardProject1">
              <template slot="cardContent">
                <badge type="rose">
                  Client: Dj Khaled
                </badge>

                <a href="javascript:void(0)">
                  <h2 class="card-title">Another One</h2>
                </a>
                <p class="card-description">
                  Don't be scared of the truth because we need to restart the
                  human foundation in truth.
                </p>
              </template>
            </full-bg-card>
          </div>
        </div>
      </div>
    </div>
    <!-- end Projects 4 -->
  </div>
</template>

<script>
import { FullBgCard, InfoAreas, Badge } from "@/components";

export default {
  components: {
    FullBgCard,
    InfoAreas,
    Badge
  },
  name: "Hp",
  data() {
    return {
      companyName: null,
      companyEmail: null,
      companyPassword: null,
      toggledClass: false,
      headerImages: {
        Image1: require("@/assets/img/bg12.jpg"),
        Image2: require("@/assets/img/examples/office2.jpg"),
        Image3: require("@/assets/img/dg1.jpg"),
        Image4: require("@/assets/img/dg2.jpg"),
        Image5: require("@/assets/img/dg3.jpg"),
      },
      cardProject: {
        cardProject1: require("@/assets/img/examples/office2.jpg"),
        cardProject2: require("@/assets/img/examples/card-blog3.jpg"),
        cardProject3: require("@/assets/img/examples/card-project6.jpg"),
      },
      cardProject2: {
        cardProject1:
          "https://s3.amazonaws.com/creativetim_bucket/products/38/original/opt_mk_thumbnail.jpg",
        cardProject2:
          "https://s3.amazonaws.com/creativetim_bucket/products/34/original/opt_lbd_pro_thumbnail.jpg",
        cardProject3:
          "http://s3.amazonaws.com/creativetim_bucket/products/26/original/opt_gsdk_new_thumbnail.jpg",
      },
      cardProject3: {
        cardProject1: require("@/assets/img/examples/card-project1.jpg"),
        cardProject2: require("@/assets/img/examples/card-project2.jpg"),
        cardProject3: require("@/assets/img/examples/card-project3.jpg"),
        cardProject4: require("@/assets/img/examples/card-project4.jpg"),
      },
      cardProject4: {
        cardProject1: require("@/assets/img/examples/card-project5.jpg"),
      },
      iphone: require("@/assets/img/sections/iphone.png"),
      iphone2: require("@/assets/img/sections/iphone2.png"),
      image: require("@/assets/img/bg9.jpg"),
    };
  },
  methods: {
    header(nr) {
      return {
        backgroundImage: `url(${this.headerImages[`Image${nr}`]})`,
      };
    },
    bodyClick() {
      let bodyClick = document.getElementById("bodyClick");

      if (bodyClick === null) {
        let body = document.querySelector("body");
        let elem = document.createElement("div");
        elem.setAttribute("id", "bodyClick");
        body.appendChild(elem);

        let bodyClick = document.getElementById("bodyClick");
        bodyClick.addEventListener("click", this.toggleNavbarMobile);
      } else {
        bodyClick.remove();
      }
    },
    toggleNavbarMobile() {
      this.NavbarStore.showNavbar = !this.NavbarStore.showNavbar;
      this.toggledClass = !this.toggledClass;
      this.bodyClick();
    },
  },
  computed: {
    features5() {
      return {
        backgroundImage: `url(${this.image})`,
      };
    },
  },
};
</script>

<style lang="scss">
.buttons {
  display: flex;
  align-items: center;
}


  div.el-carousel__container {
    height: 100vh !important;
  }
  .el-carousel {
    border-radius: 0 !important;
  }


.text-right {
  text-align: right;
}

.border-radius-0 {
  border-radius: 0;
}

.pb-0 {
  padding-bottom: 0 !important;
}
.pt-0 {
  padding-top: 0 !important;
}

@media all and (max-width: 960px) {
  .md-card-form-horizontal .md-layout-item {
    margin-top: 1.5rem;
  }
}
</style>
