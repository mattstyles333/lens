<template>
  <md-toolbar
    id="toolbar"
    md-elevation="0"
    class="md-fixed"
    :class="{
      [`md-${type}`]: !navbarTransparent,
      [extraNavClasses]: navbarTransparent,
      'md-transparent': navbarTransparent,
    }"
    :color-on-scroll="colorOnScroll"
  >
    <div class="md-toolbar-row md-collapse-lateral">
      <div class="md-toolbar-section-start">
        <md-button
          class="md-button md-button md-button-link md-white md-simple md-theme-default"
          @click="$router.push('Hp')"
        >
          <h3 class="md-title">
            {{ brand }}
          </h3>
        </md-button>
      </div>
      <div class="md-toolbar-section-end">
        <md-button
          class="md-just-icon md-simple md-toolbar-toggle"
          :class="{ toggled: toggledClass }"
          @click="toggleNavbarMobile()"
        >
          <span class="icon-bar" />
          <span class="icon-bar" />
          <span class="icon-bar" />
        </md-button>

        <div class="md-collapse">
          <div class="md-collapse-wrapper">
            <mobile-menu nav-mobile-section="false">
              <!-- Here you can add your items from the section-start of your toolbar -->
            </mobile-menu>
            <md-list>
              
              

              

              <li class="md-list-item">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean"
                >
                  <div class="md-list-item-content">
                    <md-button
                      @click="$router.push('about-us')"
                      class="md-button md-button md-button-link md-white md-simple md-theme-default"
                      ><md-icon>info</md-icon>About Us</md-button
                    >
                  </div>
                </a>
              </li>
              <li class="md-list-item">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean"
                >
                  <div class="md-list-item-content">
                    <md-button
                      @click="$router.push('product-page')"
                      class="md-success md-round"
                      ><md-icon>edit</md-icon>Cusotmize Lens</md-button
                    >
                  </div>
                </a>
              </li>
              <li class="md-list-item">
                <a
                  href="javascript:void(0)"
                  class="md-list-item-router md-list-item-container md-button-clean"
                >
                  <div class="md-list-item-content">
                    <md-button
                      @click="$router.push('shopping-cart')"
                      class="md-button md-button md-button-link md-white md-simple md-theme-default"
                      ><md-icon>shopping_basket</md-icon>Shopping
                      Cart</md-button
                    >
                  </div>
                </a>
              </li>
            </md-list>
          </div>
        </div>
      </div>
    </div>
  </md-toolbar>
</template>

<script>
let resizeTimeout;
function resizeThrottler(actualResizeHandler) {
  // ignore resize events as long as an actualResizeHandler execution is in the queue
  if (!resizeTimeout) {
    resizeTimeout = setTimeout(() => {
      resizeTimeout = null;
      actualResizeHandler();

      // The actualResizeHandler will execute at a rate of 15fps
    }, 66);
  }
}

import MobileMenu from "@/layout/MobileMenu";
export default {
  components: {
    MobileMenu,
  },
  props: {
    type: {
      type: String,
      default: "white",
      validator(value) {
        return [
          "white",
          "default",
          "primary",
          "danger",
          "success",
          "warning",
          "info",
          "dark",
        ].includes(value);
      },
    },
    colorOnScroll: {
      type: Number,
      default: 0,
    },
    navbarTransparent: {
      type: Boolean,
      default: false,
    },
  },
  data() {
    return {

      extraNavClasses: "",
      toggledClass: false,
      brand: "HOMEPAGE link",
      linksSections: [
        { name: "headers", icon: "dns" },
        { name: "features", icon: "build" },
        { name: "blogs", icon: "list" },
        { name: "teams", icon: "people" },
        { name: "projects", icon: "assignment" },
        { name: "pricing", icon: "monetization_on" },
        { name: "testimonials", icon: "chat" },
        { name: "contacts", icon: "call" },
      ],
      linksExamples: [
        { name: "About Us", href: "about-us", icon: "account_balance" },
        { name: "Blog Post", href: "blog-post", icon: "art_track" },
        { name: "Blog Posts", href: "blog-posts", icon: "view_quilt" },
        { name: "Contact Us", href: "contact-us", icon: "location_on" },
        { name: "Landing Page", href: "landing-page", icon: "view_day" },
        { name: "Login Page", href: "login-page", icon: "fingerprint" },
        { name: "Pricing Page", href: "pricing-page", icon: "attach_money" },
        {
          name: "Shopping Cart",
          href: "shopping-cart",
          icon: "shopping_basket",
        },
        { name: "Ecommerce Page", href: "ecommerce-page", icon: "store" },
        { name: "Product Page", href: "product-page", icon: "shopping_cart" },
        { name: "Profile Page", href: "profile-page", icon: "account_circle" },
        { name: "Signup Page", href: "signup-page", icon: "person_add" },
        { name: "Error Page", href: "error-page", icon: "error" },
      ],
    };
  },
  computed: {
    showDownload() {
      const excludedRoutes = ["index"];
      return excludedRoutes.every((r) => r !== this.$route.name);
    },
  },
  mounted() {
    document.addEventListener("scroll", this.scrollListener);
  },
  beforeDestroy() {
    document.removeEventListener("scroll", this.scrollListener);
  },
  methods: {
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
    handleScroll() {
      let scrollValue =
        document.body.scrollTop || document.documentElement.scrollTop;
      let navbarColor = document.getElementById("toolbar");
      this.currentScrollValue = scrollValue;
      if (this.colorOnScroll > 0 && scrollValue > this.colorOnScroll) {
        this.extraNavClasses = `md-${this.type}`;
        navbarColor.classList.remove("md-transparent");
      } else {
        if (this.extraNavClasses) {
          this.extraNavClasses = "";
          navbarColor.classList.add("md-transparent");
        }
      }
    },
    scrollListener() {
      resizeThrottler(this.handleScroll);
    },
  },
};
</script>
