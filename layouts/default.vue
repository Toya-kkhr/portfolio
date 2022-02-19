<template
>
  <v-app
  style="background: #EEEFEA;"
  >
    <v-navigation-drawer
      v-if="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm"
      v-model="drawer"
      app
      right
      dark
    >
      <v-list>
        <v-list-item
          v-for="(item) in items"
          :key="item.title"
          :v-scroll-to="item.to"
          to
          nuxt
          @click.stop="drawer = !drawer"
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
 @click.stop="drawer = !drawer"
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
 
      <v-app-bar-nav-icon
      v-if="$vuetify.breakpoint.xs || $vuetify.breakpoint.sm"
       @click.stop="drawer = !drawer" />

    <div
          v-if="$vuetify.breakpoint.md || $vuetify.breakpoint.lg || $vuetify.breakpoint.xl"
    >
      <v-btn
    v-for="(item, i) in items"
    :key="i"
    v-scroll-to="item.to"
    text
    active-class
    nuxt
      >

    {{ item.title }}
      </v-btn>
</div>
    </v-app-bar>

<v-main>
    <Nuxt/>
</v-main>

<v-footer
padless
>
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
          to: '#about'
        },
        {
          title: 'Skills',
          to: '#skills'
        },
        {
          title: 'Works',
          to: '#works'
        },
        {
          title: 'Hobbys',
          to: '#hobbys'
        },
        {
          title: 'Contact',
          to: '#contact'
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