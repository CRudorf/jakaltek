<template>
    <v-app id="inspire">
      <v-app-bar flat
        color="teal-darken-4"
        image="https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Jacaltenango..jpg/800px-Jacaltenango..jpg?20191104143250"
      >
        <template v-slot:image>
            <v-img
            gradient="to top right, rgba(15,89,21,.8), rgba(51,149,50,.8)"
            ></v-img>
        </template>
        <v-container class="fill-height d-flex align-center">
          <v-app-toolbar-title>Jakaltek</v-app-toolbar-title>
          <v-spacer></v-spacer>
          <v-btn
            v-for="link in links"
            :key="link"
            variant="text"
          >
            {{ link }}
          </v-btn>
        </v-container>
      </v-app-bar>
  
      <v-main class="bg-grey-lighten-3">
        <v-container>
          <v-row>
            <v-col cols="2">
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
            </v-col>
  
            <v-col>
              <v-sheet
                min-height="70vh"
                rounded="lg"
              >
                <!--  -->
              </v-sheet>
            </v-col>
            
          </v-row>
        </v-container>
      </v-main>
    </v-app>
  </template>
  
  <script>
    export default {
      data: () => ({
        links: [
          'Dictionary',
          'History'
        ],
      }),
    }
  </script>