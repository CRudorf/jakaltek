<template>
    <v-app id="app">
      <v-app-bar flat
        color="green-darken-4"
      >
        <template v-slot:image>
            <v-img
            gradient="to top right, rgba(15,89,21,.8), rgba(51,149,50,.8)"
            ></v-img>
        </template>
        <v-container class="fill-height d-flex align-center">
          <v-app-bar-title>Jakaltek Archives</v-app-bar-title>
          <v-spacer></v-spacer>
          <v-btn
            v-for="link in links"
            :key="link"
            class="mx-2"
            variant="outlined"
          >
            {{ link }}
          </v-btn>
        </v-container>
      </v-app-bar>
  
      <v-main class="jacaltenango-mountains">
        <v-container>
          <v-row>
            <!-- <v-col cols="2">
              <v-sheet rounded="lg">
                <v-list rounded="lg">
                  <v-list-item
                    v-for="n in 5"
                    :key="n"
                    link
                  >
                    <v-list-item-title>
                      List Item {{ n }}
                    </v-list-item-title>
                  </v-list-item>
  
                  <v-divider class="my-2"></v-divider>
  
                  <v-list-item
                    link
                    color="grey-lighten-4"
                  >
                    <v-list-item-title>
                      Refresh
                    </v-list-item-title>
                  </v-list-item>
                </v-list>
              </v-sheet>
            </v-col> -->
  
            <v-col>
              <WelcomeBanner />
            </v-col>
            
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </template>
  
  <script>

    import WelcomeBanner from './components/UnderConstructionBanner.vue'

    export default {
      components: {
        WelcomeBanner
      },
      data: () => ({
        links: [
          'Dictionary',
          'Gallery',
          'About',
          'Support'
        ],
      }),
    }
  </script>