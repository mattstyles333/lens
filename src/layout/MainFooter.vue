<template>

  <div class="wrapper">
    <!-- Image Subscribe Line -->
      <div class="md-layout">
        <div class="md-layout-item">
          <div
            class="subscribe-line subscribe-line-image"
            :style="imageSubscribe"
          >
            <div class="container">
              <div class="md-layout">
                <div
                  class="md-layout-item md-size-50 md-small-size-70 md-xsmall-size-100 mx-auto"
                >
                  <div class="text-center">
                    <h3 class="title">
                      Subscribe to our Newsletter
                    </h3>
                    <p class="description">
                      Join our newsletter and get news in your inbox every week!
                      We hate spam too, so no worries about this.
                    </p>
                  </div>
                  <md-card class="md-card-form-horizontal">
                    <md-card-content>
                      <form
                        action=""
                        method=""
                      >
                        <div class="md-layout">
                          <div
                            class="md-layout-item md-large-size-66 medium-size-50"
                          >
                            <md-field class="md-form-group">
                              <md-icon>mail</md-icon>
                              <md-input
                                v-model="subscribe"
                                placeholder="Subscribe"
                              />
                            </md-field>
                          </div>
                          <div
                            class="md-layout-item md-large-size-33 medium-size-50"
                          >
                            <md-button
                              class="md-primary md-block"
                            >
                              Subscribe
                            </md-button>
                          </div>
                        </div>
                      </form>
                    </md-card-content>
                  </md-card>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <!-- end Image Subscribe Line -->

      <!-- Big Footer -->
      <footer class="footer footer-black footer-big">
        <div class="container">
          <div class="content">
            <div class="md-layout">
              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <h5>About Us</h5>
                <p>
                  Creative Tim is a startup that creates design tools that make
                  the web development process faster and easier.
                </p>
                <p>
                  We love the web and care deeply for how users interact with a
                  digital product. We power businesses and individuals to create
                  better looking web projects around the world.
                </p>
              </div>

              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <h5>Social Feed</h5>
                <div class="social-feed">
                  <div class="feed-line">
                    <i class="fab fa-twitter" />
                    <p>
                      How to handle ethical disagreements with your clients.
                    </p>
                  </div>
                  <div class="feed-line">
                    <i class="fab fa-instagram" />
                    <p>
                      The tangible benefits of designing at 1x pixel density.
                    </p>
                  </div>
                  <div class="feed-line">
                    <i class="fab fa-facebook-square" />
                    <p>
                      A collection of 25 stunning sites that you can use for
                      inspiration.
                    </p>
                  </div>
                </div>
              </div>

              <div class="md-layout-item md-medium-size-33 md-small-size-100">
                <h5>Instagram Feed</h5>
                <div class="gallery-feed">
                  <img :src="img1" class="img img-raised rounded" alt="" />
                  <img :src="img2" class="img img-raised rounded" alt="" />
                  <img :src="img3" class="img img-raised rounded" alt="" />
                  <img :src="img4" class="img img-raised rounded" alt="" />

                  <img :src="img5" class="img img-raised rounded" alt="" />
                  <img :src="img6" class="img img-raised rounded" alt="" />
                  <img :src="img7" class="img img-raised rounded" alt="" />
                  <img :src="img8" class="img img-raised rounded" alt="" />
                </div>
              </div>
            </div>
          </div>

          <hr />

          <div class="flex flex-direction-row space-between">
            <nav>
              <ul>
                <li>
                  <a href="javascript:void(0)">
                    Blog
                  </a>
                </li>
                <li>
                  <a href="javascript:void(0)">
                    Presentation
                  </a>
                </li>
                <li>
                  <a href="javascript:void(0)">
                    Discover
                  </a>
                </li>
                <li>
                  <a href="javascript:void(0)">
                    Payment
                  </a>
                </li>
                <li>
                  <a href="javascript:void(0)">
                    Contact Us
                  </a>
                </li>
              </ul>
            </nav>
            <div class="copyright float-right">
              Copyright © {{ year }} Creative Tim All Rights Reserved.
            </div>
          </div>
        </div>
      </footer>
      <!-- end Big Footer -->
  </div>
</template>
<script>
export default {
  props: {
    backgroundColor: String,
    type: String,
    size: String
  },
  data() {
    return {
      year: new Date().getFullYear(),
      img1: require("@/assets/img/faces/card-profile6-square.jpg"),
      img2: require("@/assets/img/faces/christian.jpg"),
      img3: require("@/assets/img/faces/card-profile4-square.jpg"),
      img4: require("@/assets/img/faces/card-profile1-square.jpg"),
      img5: require("@/assets/img/faces/marc.jpg"),
      img6: require("@/assets/img/faces/kendall.jpg"),
      img7: require("@/assets/img/faces/card-profile5-square.jpg"),
      img8: require("@/assets/img/faces/card-profile2-square.jpg"),
      subscribe: null,
      image: require("@/assets/img/bg7.jpg")
    };
  },
    computed: {
    imageSubscribe() {
      return {
        backgroundImage: `url(${this.image})`
      };
    }
  }
};
</script>
<style scoped>

</style>
