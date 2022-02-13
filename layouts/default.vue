<template
>
  <v-app
  style="background: #EEEFEA;"
  >
    <v-navigation-drawer
      v-model="drawer"
      app
      right
      dark
    >
      <v-list>
        <v-list-item
          v-for="(item) in items"
          :key="item.title"
          :to="item.to"
        >
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>

      <template #append>
        <v-card
        class="text-center pa-2">
  <v-btn
 v-for="icon in icons"
 :key="icon.url"
 icon
  :href="icon.url"
 target="_blank"
 >
   <v-icon>
     {{ icon.icon }}
   </v-icon>
 </v-btn>
        </v-card>
      </template>
     </v-navigation-drawer>

    <v-app-bar 
    style=
    " background-color: rgba(0, 0, 0, 0);
    " 
    fixed
    flat
    >

      <v-spacer />
 
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" />

    </v-app-bar>
      <v-main>

<hero-view />

  <div
  id="about"
  class="mb-5"
  >
  <v-container>
    <aboutView />
  </v-container>
  </div>

  <div
  id="skills"
  style="background: #E0E1DB;"
    class="mb-5"
  >
  <v-container>
    <skills-view />
  </v-container>
  </div>

<div
id="works"
  class="mb-5"
>
  <v-container>
    <works-view />
  </v-container>
</div>

<div
id="hobbys"
  class="mb-5"
>
    <v-container
      style="background: #E0E1DB;"
    >
    <hobbys-view />
  </v-container>
</div>

<div
id="contact"
  class="mb-5"
>
    <v-container>
    <contact-view />
  </v-container>
</div>

      </v-main>
  <v-footer padless>
 <v-card
 width="100%"
 class="text-center"
 style="background: #E0E1DB;"
 flat
 tile
 >

 <v-btn
 v-for="icon in icons"
 :key="icon.icon"
 icon
 :href="icon.url"
 target="_blank"
 >
   <v-icon>
     {{ icon.icon }}
   </v-icon>
 </v-btn>

<v-divider></v-divider>

           <v-card-text>
          {{ new Date().getFullYear() }} — <strong>Toya Kakohara</strong>
        </v-card-text>
 </v-card>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      drawer: false,
      items: [
        {
          title: 'About',
          to: '#about',
        },
        {
          title: 'Skills',
          to: '#skills',
        },
        {
          title: 'Works',
          to: '#works',
        },
        {
          title: 'Hobbys',
          to: '#hobbys',
        },
        {
          title: 'Contact',
          to: '#contact',
        },
      ],

      icons: [
        {
          icon: "mdi-facebook",
          url: "https://www.facebook.com/touya.kakohara/"
        },
        { 
          icon: "mdi-instagram",
          url: "https://www.instagram.com/__toya1128/"
        },
        {
         icon: "mdi-github",
         url: "https://github.com/Toya-kkhr/"
        }

      ]
    }
  },
}
</script>

<style lang="scss">
</style> 