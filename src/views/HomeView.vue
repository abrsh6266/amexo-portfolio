<template>
  <v-app id="home">
    <Navbar />
    <v-container fluid>
      <div class="head">
        <v-row>
          <v-col cols="5">
            <div style="position: relative" class="mt-16">
              <h1 class="text-grey">Hello,</h1>
              <h1 class="text-white">I'M Amare </h1>
              <span class="text-grey">Visual Artist & painter</span><br />

              <v-btn tile dark class="text-yellow mt-8" variant="outlined">
                Contact me
              </v-btn>
            </div>
          </v-col>
          <v-col cols="2">
            <div style="
                position: absolute;
                z-index: 9999;
                bottom: 0;
                margin-left: auto;
                margin-right: auto;
                left: 0;
                right: 0;
                text-align: center;
              " class="mt-16">
              <v-icon>fas fa-angle-double-down</v-icon>
            </div>
          </v-col>
          <v-col cols="5">
            <div style="position: relative; z-index: 9999" class="mt-16">
              <v-img src="ami2.jpg" contain max-height="300"></v-img>
            </div>
          </v-col>
        </v-row>
      </div>
      <v-col cols="12" class="mt-16" id="about">
        <div>
          <v-row>
            <v-col cols="12" sm="6">
              <div class="egg">
                <v-img src="ami2.jpg" max-height="300" class=""></v-img>
              </div>
            </v-col>
            <v-col cols="12" sm="6">
              <h1 class="mt-16 mb-6">About Me</h1>
              <h4 class="mt-n4">I Am a Creative Visual Artist</h4>
              <p class="text-grey">
                I am Amare Teshome, a visual artist who graduated in 2024 from Addis Ababa University's Alle School of
                Fine Arts and Design with a degree in painting. Over four years, I studied a wide range of visual art
                courses, gaining extensive knowledge and wisdom about visual art and artists.
              </p>
              <br />
              <p class="text-grey">
                I now have experience in various visual art categories, including realism, abstraction,
                semi-abstraction, mural painting, ceramic
                mosaics, landscape painting, figurative art, and drawing.
              </p>
              <!-- <v-btn tile dark color="yellow" class="mt-4">
                Download Resume
              </v-btn> -->
            </v-col>
          </v-row>
        </div>
      </v-col>
      <div class="text-center mt-4">
        <h2>What I Do</h2>
      </div>
      <v-col cols="12" class="padd" id="portfolio">
        <div class="first" id="project">
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-paint-brush" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Painting</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I create expressive artworks using various <br />mediums like oil, acrylic, and watercolor on surfaces
                  <br />such as canvas, wood, or paper.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-pencil-alt" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Drawing</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I use pencils, pens, and charcoal to produce <br />detailed representations and conceptual sketches
                  <br />on paper.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-palette" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Mural</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I design and paint large-scale artworks <br />directly on walls or ceilings, enhancing public
                  <br />and private spaces with vibrant visuals.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-row>
            <v-col cols="12">
              <div class="child">
                <v-btn icon="fas fa-th" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Ceramic Mosaic</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I arrange and fix small pieces of colored <br />ceramics or tiles to create intricate patterns
                  <br />and images on various surfaces.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-mountain" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Landscape Painting</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I capture the beauty of natural scenery, <br />portraying mountains, valleys, trees, and rivers
                  <br />to reflect the essence of the outdoors.
                </p>
              </div>
              <div class="child">
                <v-btn icon="fas fa-random" color="#FBDF7E" class="text-white"></v-btn>
                <h3 class="ml-3 mt-4">Abstract Painting</h3>
                <p class="text-grey ml-3 mt-4 text-caption">
                  I use shapes, colors, and gestural marks to <br />create artworks that focus on emotional
                  <br />and conceptual experiences.
                </p>
              </div>
            </v-col>
          </v-row>
          <v-divider></v-divider>
        </div>
      </v-col>
      <v-col cols="12" sm="12" id="services">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mr-2">All</v-btn>
          <v-btn class="mr-2" variant="tonal">Painting</v-btn>
          <v-btn class="mr-2" variant="tonal">Drawing</v-btn>
          <v-btn class="mr-2" variant="tonal">Mural</v-btn>
          <v-btn class="mr-2" variant="tonal">Ceramic Mosaic</v-btn>
          <v-btn class="mr-2" variant="tonal">Landscape Painting</v-btn>
          <v-btn variant="tonal">Abstract Painting</v-btn>
        </div>
      </v-col>

      <v-col cols="12" class="imgHover">
        <v-row class="fill-height" align="center" justify="center">
          <template v-for="(item, i) in items" :key="i">
            <v-col cols="12" md="4">
              <v-hover v-slot="{ isHovering, props }">
                <v-card :elevation="isHovering ? 12 : 2" :class="{ 'on-hover': isHovering }" v-bind="props">
                  <v-img :src="item.img" height="225px" cover> </v-img>
                </v-card>
              </v-hover>
            </v-col>
          </template>
        </v-row>
      </v-col>
      <v-col cols="12" sm="12">
        <div class="d-flex justify-center mb-6">
          <v-btn color="#FBDF7E" class="mt-4">Explore all my Works</v-btn>
        </div>
      </v-col>
      <v-col cols="12" id="page">
        <div class="pre">
          <v-row>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="painting.jpg" height="200px" cover></v-img>

                <v-card-title>Painting</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | march 2024
                </v-card-subtitle>
                <v-card-text>
                  Create expressive artworks using various mediums like oil, acrylic, and watercolor on surfaces such as
                  canvas, wood, or paper.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="drawing.jpg" height="200px" cover></v-img>

                <v-card-title>Drawing</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | July 2022
                </v-card-subtitle>
                <v-card-text>
                  Produce detailed representations and conceptual sketches using pencils, pens, and charcoal on paper.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="mural.jpg" height="200px" cover></v-img>

                <v-card-title>Mural</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | May 2023
                </v-card-subtitle>
                <v-card-text>
                  Design and paint large-scale artworks directly on walls or ceilings, enhancing public and private
                  spaces
                  with vibrant visuals.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="mosaic.png" height="200px" cover></v-img>

                <v-card-title>Ceramic Mosaic</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | October 2024
                </v-card-subtitle>
                <v-card-text>
                  Arrange and fix small pieces of colored ceramics or tiles to create intricate patterns and images on
                  various
                  surfaces.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="landscape.jpg" height="200px" cover></v-img>

                <v-card-title>Landscape Painting</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | January 2021
                </v-card-subtitle>
                <v-card-text>
                  Capture the beauty of natural scenery, portraying mountains, valleys, trees, and rivers to reflect the
                  essence of the outdoors.
                </v-card-text>
              </v-card>
            </v-col>
            <v-col cols="12" sm="4">
              <v-card class="mx-auto" max-width="344" height="">
                <v-img src="abstract.jpg" height="200px" cover></v-img>

                <v-card-title>Abstract Painting</v-card-title>

                <v-card-subtitle>
                  By Amare Teshome | February 2024
                </v-card-subtitle>
                <v-card-text>
                  Use shapes, colors, and gestural marks to create artworks that focus on emotional and conceptual
                  experiences.
                </v-card-text>
              </v-card>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <v-col cols="12" id="biog">
        <div class="hire">
          <v-row>
            <v-col cols="12" sm="8">
              <h1 class="mt-9">Commission Artwork or Collaborate</h1>
              <p class="text-grey">
                Whether you need a custom painting, mural, ceramic mosaic, or other artistic collaboration, I'm ready to
                bring
                your vision to life with creativity and passion.
              </p>
            </v-col>
            <v-col cols="12" sm="4">
              <v-btn color="#FBDF7E" class="mt-15">Hire Me</v-btn>
            </v-col>
          </v-row>
        </div>
      </v-col>

      <v-col cols="12" sm="12" class="px-16" id="contact">
        <v-row>
          <v-col cols="12" sm="4">
            <div class="child">
              <h1>Contact Info</h1>
              <v-btn icon="fas fa-map-marker-alt" color="" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">Addis Ababa, 4 Kilo Street</span><br />
              <v-btn icon="fas fa-phone-alt" color="" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">+251 - 947082270</span><br />
              <span class="text-caption">+251 - 777082270</span><br />
              <v-btn icon="fas fa-envelope" color="" class="mt-10" variant="outlined"></v-btn><br />
              <span class="text-caption">amarearts12@gmail.com</span><br />
              <span class="text-caption">myartamare@gmail.com</span><br />
            </div>
          </v-col>
          <v-col cols="12" sm="8">
            <h1 class="mt-8">Send Your Message</h1>
            <v-divider></v-divider>
            <span class="text-caption">Have a project in mind or want to discuss a collaboration? Feel free to reach
              out!</span>
            <v-row class="mt-10">
              <v-col cols="12" sm="6">
                <v-text-field label="Name" persistent-hint variant="outlined"></v-text-field>
              </v-col>
              <v-col cols="12" sm="6">
                <v-text-field label="Phone No" persistent-hint variant="outlined"></v-text-field>
              </v-col>
            </v-row>
            <v-textarea label="Message" persistent-hint variant="outlined"></v-textarea>
            <v-btn color="#FBDF7E" class="mt-2">Submit Now</v-btn>
          </v-col>
        </v-row>
      </v-col>

    </v-container>
    <FooterView />
  </v-app>
</template>

<script>
import { defineComponent } from "vue";
import FooterView from "../components/FooterView.vue";
import Navbar from "@/components/Navbar.vue";

// Components
//import HelloWorld from '../components/HelloWorld.vue';

export default defineComponent({
  name: "HomeView",
  setup() {
    return {
      slider2: 50,

      items: [
        {
          img: "i3.jpg",
        },
        {
          img: "i4.jpg",
        },
        {
          img: "i5.jpg",
        },
        {
          img: "i6.jpg",
        },
        {
          img: "i9.png",
        },
        {
          img: "i8.jpg",
        },
        {
          img: "i10.jpg",
        },
        {
          img: "i11.jpg",
        },

      ],
    };
  },
  components: {
    Navbar,
    FooterView
  },
});
</script>
<style scoped>
.v-container {
  padding: 16px 0 16px 0;
}

.head {
  position: relative;
  text-align: center;
  padding: 12px;
  margin-bottom: 6px;
  height: 400px;
  width: 100%;
  color: white;
}

.head:before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, 6deg);
}

.head:after {
  content: "";
  position: absolute;
  top: 0;
  right: 0;
  height: 100%;
  width: 50%;
  background: black;
  transform: skew(0deg, -6deg);
}

.egg {
  display: block;
  margin-left: 100px;
  margin-top: 50px;
  width: 356px;
  height: 300px;
  background-color: #fbdf7e;
  border-radius: 50% 50% 50% 50% / 60% 60% 40% 40%;
}

.first {
  width: 100%;
  height: 560px;
  text-align: center;
  padding: 2rem 2rem;
}

.child {
  display: inline-block;
  padding: 2rem 1rem;
  vertical-align: middle;
  text-align: center;
  margin-right: 8px;
}

.imgHover {
  padding: 0 200px;
}

.pre {
  width: 100%;
  height: 760px;
  text-align: center;
  padding: 0 200px;
  background-color: #f5f5f5;
}

.hire {
  width: 100%;
  height: 200px;
  padding: 0 200px;
  background-color: #e9e9e9;
  margin-top: -24px;
}
</style>