<template>
    <v-app
      style="background: #EEEFEA;"
    >
        <v-main>
        <success/>
        </v-main>
        
<v-footer
padless
fixed
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
import success from '../pages/success.vue'
export default {
    name: "OtherLayout",
  components: { success },
  data() {
      return {
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
  }
}
</script>