<template>
  <div>
    <q-header bordered class="desktop-view bg-white">
      <div class="row">
        <div class="col-lg-1 col-md-1 col-sm-1 col-xs-1"></div>
        <div class="col-lg-9 col-md-9 col-sm-9 col-xs-9">
          <q-toolbar class="top-header-rpl">
            <div class="redimind-img-div-rpl">
              <img
                src="../assets/Vault-Logo.webp"
                style="height: 45px; cursor: pointer; padding-top: 5px"
              />
            </div>
            <q-space />

            <q-toolbar-title>
              <div class="title-block">
                <div class="home" :style="{ color: navbarColors[$route.path] }">
                  {{ Navigation1 }}
                </div>
                <div
                  class="about"
                  :style="{ color: navbarColors1[$route.path] }"
                >
                  {{ Navigation2 }}
                </div>
                <div class="services">
                  <q-btn-dropdown
                    flat
                    no-caps
                    style="position: relative"
                    label="Services"
                  >
                    <q-list>
                      <q-item clickable v-close-popup @click="onItemClick">
                        <q-item-section>
                          <q-item-label>Photos</q-item-label>
                        </q-item-section>
                      </q-item>

                      <q-item clickable v-close-popup @click="onItemClick">
                        <q-item-section>
                          <q-item-label>Videos</q-item-label>
                        </q-item-section>
                      </q-item>

                      <q-item clickable v-close-popup @click="onItemClick">
                        <q-item-section>
                          <q-item-label>Articles</q-item-label>
                        </q-item-section>
                      </q-item>
                    </q-list>
                  </q-btn-dropdown>
                </div>
                <div
                  class="Blog"
                  :style="{ color: navbarColors3[$route.path] }"
                >
                  Blog
                </div>
                <div
                  class="Learn"
                  :style="{ color: navbarColors4[$route.path] }"
                >
                  Contact
                </div>
              </div>
            </q-toolbar-title>
          </q-toolbar>
        </div>
        <div class="col-lg-2 col-md-2 col-sm-2 col-xs-2">
          <q-toolbar>
            <q-btn
              color="black"
              label="Get in Touch"
              icon="mail"
              no-caps
              size="md"
              style="position: absolute; top: 7px; left: 15px"
            ></q-btn>
          </q-toolbar>
        </div>
      </div>
    </q-header>
    <q-header bordered class="mobile-view-rpl bg-white">
      <q-toolbar class="top-header-rpl q-px-sm">
        <div>
          <img
            src="../assets/ayasya-logo.png"
            style="height: 30px"
            @click="scrollToElementmb('home-mb')"
          />
        </div>
        <q-space />
        <div id="mySidenav" class="sidenav">
          <a class="closebtn" @click="closeNav()">&times;</a>

          <a @click="scrollToElementmb('id_Home_mb')">Home</a>
          <a @click="scrollToElementmb('id_About Us')">About Us</a>
          <a @click="scrollToElementmb('id_Services_mb')">Services</a>
          <a @click="scrollToElementmb('id_Blog_mb')">Blog</a>
          <a @click="scrollToElementmb('id_Contact_mb')">Contact</a>
        </div>
        <q-btn size="md" flat icon="menu" @click="openNav()" color="black" />
      </q-toolbar>
    </q-header>

    <!-- Desktop-design -->
    <div class="row">
      <div class="col-lg-1 col-md-1 col-sm-1"></div>
      <div class="col-lg-10 col-md-10 col-sm-10">
        <div class="row">
          <div class="col-lg-6 col-md-6 col-sm-6">
            <div
              class="headline-text"
              style="padding-top: 120px; padding-right: 65px"
            >
              Creating the best digital solutions for your business
            </div>

            <p class="quote">
              Amet, fames enim vel nec elit aliquet vestibulum vitae tempus.
              Lacus adipiscing vitae, aliquet lorem. Praesent nulla consequat
              mauris, tristique elementum, aenean enim.
            </p>
            <q-btn
              color="black"
              label="Get in Touch"
              no-caps
              size="lg"
              style="position: relative; top: 30px; left: 95px"
            ></q-btn>
            <q-btn
              color="white"
              text-color="black"
              icon="play_circle"
              label="Watch Video"
              target="_blank"
              type="a"
              href="https://www.youtube.com/watch?v=PHe0bXAIuk0&t=8s&ab_channel=PrinciplesbyRayDalio"
              no-caps
              size="lg"
              style="position: relative; top: 30px; left: 120px"
            ></q-btn>
          </div>

          <div class="col-lg-6 col-md-6 col-sm-6">
            <img
              src="../assets/corporate.png"
              style="padding: 95px 0px 0px 90px"
            />
            <p>{{ Navigation1 }}</p>
            <p>{{ Navigation2 }}</p>
          </div>
        </div>

        <div
          class="q-py-lg"
          style="display: flex; align-items: center; justify-content: center"
        >
          <button class="learn-more">
            <span class="circle" aria-hidden="true">
              <span class="icon arrow"></span>
            </span>
            <span class="button-text">Learn More</span>
          </button>
        </div>

        <div class="row">
          <div class="col-lg-8 col-md-8 col-sm-8">
            <div
              class="headline-text1"
              style="padding-top: 80px; padding-right: 45px"
            >
              We’ve worked on over 200 projects with 150+ clients
            </div>

            <p class="quote1">
              Velit platea dolor tristique hendrerit vel morbi. Ac porta
              malesuada sed phasellus. Gravida senectus at diam risus, enim
              etiam. Lectus sed eu mus.
            </p>
          </div>
        </div>

        <div class="row">
          <div class="col-lg-12 col-md-12 col-sm-12 col-xs-12">
            <div class="one">
              <img
                src="../assets/Corporate-logo-1.webp"
                width="20%"
                alt="Null"
                style="padding: 45px 10px 0px 90px"
              />
              <img
                src="../assets/Corporate-logo-2.webp"
                width="20%"
                alt="Null"
                style="padding: 45px 10px 0px 90px"
              />
              <img
                src="../assets/Corporate-logo-3.webp"
                width="20%"
                alt="Null"
                style="padding: 45px 10px 0px 90px"
              />
              <img
                src="../assets/Corporate-logo-4.webp"
                width="20%"
                alt="Null"
                style="padding: 45px 10px 0px 90px"
              />
              <img
                src="../assets/Corporate-logo-5.webp"
                width="20%"
                alt="Null"
                style="padding: 45px 10px 0px 90px"
              />
            </div>
          </div>
        </div>

        <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl">
          <div class="q-pa-md">
            <div class="q-col-gutter-md row">
              <div
                class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center"
              >
                <img
                  src="../assets/corporate1.png"
                  style="padding: 95px 0px 0px 0px"
                />
              </div>

              <div
                class="col-md-6 col-md-6 col-xs-12 col-sm-12 text-center flex flex-center"
              >
                <div
                  class="headline-text2"
                  style="padding-top: 120px; padding-left: 65px"
                >
                  Embracing technology, enhanching people's lives
                </div>

                <p class="quote2">
                  Proin in mauris scelerisque risus nisl cras. Non dui nec vitae
                  nunc. Nulla egestas platea urna in. Vitae augue pulvinar
                  vitae, platea risus est. Gravida vel tempor, ut odio est
                  elementum viverra. Praesent nulla consequat mauris, tristique
                  elementum, aenean enim.Ac porta malesuada sed phasellus.
                  Gravida senectus at diam risus, enim etiam. Lectus sed eu mus.
                </p>
                <hr style="width: 82%; margin-right: 25px" />
                <div class="Api-icon" style="padding-left: 45px">
                  <i class="fas fa-cubes fa-lg">
                    <span class="headline-Api"> API Integration </span>
                  </i>
                  <p class="Api-Quote">
                    Velit condimentum integer lectus ipsum condimentum auctor
                    eget. Metus nec lorem tempor euismod pretium leo, ipsum odio
                    curabitur.
                  </p>
                </div>
                <div
                  class="Business-icon"
                  style="padding-bottom: 30px; padding-left: 45px"
                >
                  <i class="fas fa-store fa-lg">
                    <span class="headline-Business"> Business Continuity </span>
                  </i>
                  <p class="Business-Quote">
                    Diam neque feugiat vulputate lorem ut congue et euismod.
                    Purus laoreet tortor dictum vivamus metus enim ac.
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>

        <div
          style="
            height: 2000px;
            padding-top: 40px;
            background-color: #101828;
            z-index: 0;
          "
          class="content"
        >
          <div class="row row q-px-xl">
            <div
              class="text-h4 text-center text-white q-py-sm q-my-md full-width Solutions-text"
            >
              Our Solutions
              <div style="position: sticky; padding: 0px 190px 0px 180px">
                <p class="Solutions-quote">
                  Proin in mauris scelerisque risus nisl cras. Non dui nec vitae
                  nunc. Nulla egestas platea urna in. Vitae augue pulvinar
                  vitae, platea risus est. Gravida vel tempor, ut
                </p>
              </div>
            </div>
            <div class="col-md-12 col-md-12 col-xs-12 col-sm-12 q-mb-xl">
              <div class="q-pa-md">
                <div class="q-col-gutter-md row"></div>

                <div class="row">
                  <div class="col-lg-2 col-md-2 col-sm-2"></div>
                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/user.png"
                        style="width: 25%; margin-left: 50px"
                      />
                    </div>
                    <div
                      class="talent-text1"
                      style="padding-top: 20px; padding-right: 15px"
                    >
                      Talent Acquisition
                    </div>
                    <p class="talent-quote1">
                      Pulvinar proin imperdiet malesuada <br />fermentum. In
                      egestas nec duis <br />fames ultricies tempus.
                    </p>
                  </div>

                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/IT Governance.png"
                        style="width: 25%; margin-left: 70px"
                      />
                    </div>
                    <div
                      class="talent-text2"
                      style="padding-top: 20px; margin-left: 30px"
                    >
                      IT Governance
                    </div>
                    <p class="talent-quote2">
                      Vehicula nunc tellus metus, eget. Vel, urna et sed
                      porttitor.
                    </p>
                  </div>

                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/Digital Transformation.png"
                        style="width: 25%; margin-left: 95px"
                      />
                    </div>
                    <div
                      class="talent-text3"
                      style="padding-top: 20px; margin-left: 20px"
                    >
                      Digital Transformation
                    </div>
                    <p class="talent-quote3">
                      Id phasellus ut venenatis eleifend turpis. Blandit ut a
                      vitae, accumsan tristique eu viverra arcu cursus.
                    </p>
                  </div>
                </div>
                <div class="col-lg-1 col-md-1 col-sm-1"></div>

                <div class="row">
                  <div class="col-lg-2 col-md-2 col-sm-2"></div>
                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/Data Management & Security.png"
                        style="width: 28%; margin-left: 50px"
                      />
                    </div>
                    <div
                      class="talent-text4"
                      style="padding-top: 20px; margin-left: -45px"
                    >
                      Data Management & Security
                    </div>
                    <p class="talent-quote4">
                      Risus risus mattis mattis risus<br />
                      portitor. Proin vel, sapien odio arcu, <br />odio.
                    </p>
                  </div>

                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/api.png"
                        style="width: 27%; margin-left: 70px; margin-top: 10px"
                      />
                    </div>
                    <div
                      class="talent-text5"
                      style="padding-top: 15px; margin-left: 10px"
                    >
                      Request API Integration
                    </div>
                    <p class="talent-quote5">
                      Sit tortor nunc aenean faucibus<br />
                      dignissim duis leo orn.
                    </p>
                  </div>

                  <div class="col-lg-3 col-md-3 col-sm-3">
                    <div class="row">
                      <img
                        src="../assets/database.png"
                        style="width: 29%; margin-left: 95px; margin-top: 10px"
                      />
                    </div>
                    <div
                      class="talent-text6"
                      style="padding-top: 10px; margin-left: 30px"
                    >
                      Big Data Manipulation
                    </div>
                    <p class="talent-quote6">
                      Diam nam sit nibh felis sed vel at eget. Ut ultrices at
                      montes.
                    </p>
                  </div>
                </div>
                <div class="col-lg-1 col-md-1 col-sm-1"></div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="col-lg-1 col-md-1 col-sm-1"></div>
    </div>
  </div>
</template>

<script>
import { scroll } from "quasar";
import corporatejson from "../views/data/corporate.json";

export default {
  created() {},
  computed: {},
  data() {
    let homeData;
    let aboutUsData;

    corporatejson.navbar.forEach((item) => {
      console.log("Nav-item", item.Home);
      homeData = item.Home;
      console.log("Navigation-Data : ", homeData);

      console.log("Nav-item", item.AboutUs);
      aboutUsData = item.AboutUs;
      console.log("Navigation-Data : ", aboutUsData);
    });

    return {
      Navigation1: homeData,
      Navigation2: aboutUsData,

      navbarColors: {
        "/websiteHome": "orange",
      },
      navbarColors1: {
        "/aboutUs": "orange",
      },
      navbarColors2: {
        "/blogs": "orange",
      },
      navbarColors3: {
        "/learnmore": "orange",
      },
      navbarColors4: {
        "/learnmore": "orange",
      },
    };
  },
  methods: {
    onItemClick() {
      console.log("Welcome");
    },
    watchVideoLink() {
      this.$router.push("https://vault.uicore.co/corporate/");
    },

    openNav() {
      document.getElementById("mySidenav").style.width = "250px";
    },
    closeNav() {
      document.getElementById("mySidenav").style.width = "0";
    },
  },
};
</script>

<style lang="scss" scoped>
$blue-color: #00d1c1;
$black-color: #00160a;

.top-header-rpl {
  color: black;
  background: white;
}

.title-block {
  display: flex;
  justify-content: space-between;
  font-size: 16px;
}

.headline-text {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
  color: #1a242e;
  font-size: 80px;
  font-weight: 600;
  text-transform: initial;
  line-height: 1em;
  padding-bottom: 0.5em;
  margin-bottom: 0;
}

.headline-text1 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  text-align: center;
  color: #1a242e;
  font-size: 28px;
  font-weight: bold;
  text-transform: initial;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.headline-text2 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  text-align: left;
  color: #1a242e;
  font-size: 40px;
  font-weight: 600;
  text-transform: initial;
  line-height: 1em;
}
.headline-Api {
  font-family: Arial, Helvetica, sans-serif;
  padding-right: 310px;
  padding-left: 8px;
  font-size: 15px;
  font-weight: bold;
}
.headline-Business {
  font-family: Arial, Helvetica, sans-serif;
  padding-right: 270px;
  padding-left: 8px;
  font-size: 15px;
  font-weight: bold;
}
.Solutions-text {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 45px;
  line-height: 1em;
}
.talent-text1 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 21px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.talent-text2 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 21px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.talent-text3 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 21px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.talent-text4 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 19px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.talent-text5 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 19px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.talent-text6 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  color: whitesmoke;
  font-size: 19px;
  font-weight: 500;
  line-height: 1em;
  padding-bottom: 0.5em;
}
.quote {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 16px;
  font-weight: 10px;
  margin-top: 10px;
  text-align: center;
  text-transform: initial;
  padding-right: 40px;
  padding-left: 30px;
  margin-bottom: 0;
  display: inline-block;
}
.quote1 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 18px;
  font-weight: 10;
  margin-top: 10px;
  text-transform: initial;
  padding-right: 40px;
  padding-left: 10px;
  display: inline-block;
}
.quote2 {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.1em;
  text-transform: initial;
  padding-left: 70px;
  display: inline-block;
  text-align: left;
}
.Api-Quote {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.1em;
  margin-top: 10px;
  text-transform: initial;
  padding-left: 20px;
  display: inline-block;
  text-align: left;
}
.Business-Quote {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.1em;
  margin-top: 10px;
  text-transform: initial;
  padding-left: 20px;
  display: inline-block;
  text-align: left;
}
.Solutions-quote {
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 17px;
  margin-top: 10px;
  color: whitesmoke;
  padding-top: 15px;
  text-align: center;
  color: #ffffff9c;
  line-height: 1.5em;
}
.talent-quote1 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 10px;
  text-transform: initial;
  margin-left: -40px;
  display: inline-block;
  text-align: center;
}
.talent-quote2 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 10px;
  text-transform: initial;
  margin-left: -18px;
  display: inline-block;
  text-align: center;
}
.talent-quote3 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 10px;
  text-transform: initial;
  padding-left: 10px;
  display: inline-block;
  text-align: center;
}
.talent-quote4 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 10px;
  text-transform: initial;
  margin-left: -60px;
  display: inline-block;
  text-align: center;
}
.talent-quote5 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 5px;
  text-transform: initial;
  margin-left: 2px;
  display: inline-block;
  text-align: center;
}
.talent-quote6 {
  color: #ffffff9c;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
  font-size: 1.2em;
  margin-top: 7px;
  text-transform: initial;
  margin-left: 12px;
  display: inline-block;
  text-align: center;
}

button {
  position: relative;
  display: inline-block;
  cursor: pointer;
  outline: none;
  border: 0;
  vertical-align: middle;
  text-decoration: none;
  background: transparent;
  padding: 0;
  font-size: inherit;
  font-family: inherit;
}

button.learn-more {
  width: 12rem;
  height: auto;
}

button.learn-more .circle {
  transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
  position: relative;
  display: block;
  margin: 0;
  width: 3rem;
  height: 3rem;
  background: #282936;
  border-radius: 1.625rem;
}

button.learn-more .circle .icon {
  transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
  position: absolute;
  top: 0;
  bottom: 0;
  margin: auto;
  background: #fff;
}

button.learn-more .circle .icon.arrow {
  transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
  left: 0.625rem;
  width: 1.125rem;
  height: 0.125rem;
  background: none;
}

button.learn-more .circle .icon.arrow::before {
  position: absolute;
  content: "";
  top: -0.29rem;
  right: 0.0625rem;
  width: 0.625rem;
  height: 0.625rem;
  border-top: 0.125rem solid #fff;
  border-right: 0.125rem solid #fff;
  transform: rotate(45deg);
}

button.learn-more .button-text {
  transition: all 0.45s cubic-bezier(0.65, 0, 0.076, 1);
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  padding: 0.75rem 0;
  margin: 0 0 0 1.85rem;
  color: #282936;
  font-weight: 700;
  line-height: 1.6;
  text-align: center;
  text-transform: uppercase;
}

button:hover .circle {
  width: 100%;
}

button:hover .circle .icon.arrow {
  background: #fff;
  transform: translate(1rem, 0);
}

button:hover .button-text {
  color: #fff;
}

.carousel-text1 {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  font-size: 1.5rem;
  line-height: 1.3em;
}

.carousel-text2 {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  font-size: 1.5rem;
  line-height: 1.3em;
}

.carousel-text3 {
  font-family: Verdana, Geneva, Tahoma, sans-serif;
  font-weight: 400;
  text-transform: uppercase;
  font-size: 1.5rem;
  line-height: 1.3em;
}

.card-design {
  display: flex;
  justify-content: center;
  align-items: center;
}

.my-card {
  border-radius: 20px;
  width: 420px;
  height: 500px;
  margin: 20px 45px;
}

.home {
  color: $black-color;
  font-weight: 500;
  padding-top: 15px;
  padding-left: 15px;
}

.home:hover {
  color: #00d1c1;
  cursor: pointer;
}

.about {
  color: $black-color;
  font-weight: 500;
  padding-top: 15px;
  padding-left: 15px;
}

.about:hover {
  color: #00d1c1;
  cursor: pointer;
}

.services {
  color: $black-color;
  padding-top: 6px;
}

.services:hover {
  color: #00d1c1;
  cursor: pointer;
}

.Blog {
  color: $black-color;
  font-weight: 500;
  padding-top: 15px;
  padding-right: 8px;
}

.Blog:hover {
  color: #00d1c1;
  cursor: pointer;
}

.Learn {
  color: $black-color;
  font-weight: 500;
  padding-top: 15px;
  padding-left: 15px;
}

.Learn:hover {
  color: #00d1c1;
  cursor: pointer;
}

.login-button {
  background: $blue-color !important;
  color: white !important;
}

.item-border-rpl {
  border: 1px solid $blue-color;
  border-radius: 10px;
}

@media (min-width: 600px) and (max-width: 767px) {
  .title-block {
    font-size: 7px;
  }
}

@media (min-width: 768px) and (max-width: 1023px) {
  .title-block {
    font-size: 10px;
  }
}

@media (min-width: 1024px) and (max-width: 1439px) {
}

@media (min-width: 1440px) and (max-width: 1919px) {
  .title-block {
    font-size: 18px;
  }
}

@media (min-width: 1920px) {
  .title-block {
    font-size: 22px;
  }
}

.sidenav {
  height: 60%;
  width: 0;
  position: fixed;
  z-index: 1;
  top: 0;
  right: 0;
  background-color: #00d1c1;
  overflow-x: hidden;
  transition: 0.5s;
  padding-top: 60px;
}

.sidenav a {
  padding: 8px 8px 8px 32px;
  text-decoration: none;
  font-size: 20px;
  color: #ffffff;
  display: block;
  transition: 0.3s;
}

.sidenav a:hover {
  color: #00d1c1;
}

.sidenav .closebtn {
  position: absolute;
  top: 0;
  right: 25px;
  font-size: 36px;
  margin-left: 50px;
}

@media all and (max-width: 599px) {
  .mobile-view-rpl {
    display: block;
  }

  .desktop-view {
    display: none;
  }
}

@media all and (min-width: 600px) {
  .mobile-view-rpl {
    display: none;
  }

  .desktop-view {
    display: block;
  }
}

.main {
  -webkit-background-size: cover;
  -moz-background-size: cover;
  -o-background-size: cover;
  background-size: cover;
  height: 100vh !important;
}
</style>
