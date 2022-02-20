<template>
    <v-row
    align="center"
    justify="center"
    >
        <v-col
        align="center"
        cols="12"
        sm="6"
        >
        <div
        class="pa-3"
        >
        <h2
        style="text-decoration: underline;"
        >
            Works
        </h2>
    </div>

    <div>
        <v-card
        v-for="(work, i) in items"
        :key="i"
        class="ma-5"
        hover
        raised
        elevation-20
        @click="openDialog(work)"
        >
                                    
            <v-img
            :src= "work.image"
            :lazy-src="work.lazy"
            >
            </v-img> 
                    <v-card-title>
            {{ work.title }}
        </v-card-title>

            <v-card-text>
                {{ work.skill }}
            </v-card-text>
        </v-card>

        <v-dialog
        v-if="currentWork"
        v-model="dialog"
        max-width="700px"
        >
          <v-card>

              <v-col
              align="center"
              >
                <v-img
                :src="currentWork.image"
                :lazy-src="currentWork.lazy"
                max-width="500px"
                > 
                </v-img>
                      </v-col>

                <v-card-title>
                    {{ currentWork.title }}
                </v-card-title>
                <v-card-text>
                    {{ currentWork.skill }}
                </v-card-text>
                <div
                class="pa-10 text-center"
                >
                    {{ currentWork.exp }}
                </div>
                <div
                >
                <v-card-actions>
                    <v-btn
                    width="100%"
                    color="grey darken-1"
                    style="color:white;"
                    :href="currentWork.url"
                    target="_blank"
                    height="50px"
                    >
                        サイトを見る
                    </v-btn>
                </v-card-actions>
                </div>
            </v-card>
        </v-dialog>
    </div>

        </v-col>
    </v-row>
</template>

<script>
export default {
    name: "WorksPage",
    data() {
        return {
            dialog: false,
            currentWork: "",
            overlay: true,
            items: [
                {
                    title: "Bluwm LP",
                     image: "/bluwm-img.webp",
                     lazy: "/bluwm-lazy.webp",
                     skill: "Vue.js/ Nuxt.js/ Netlify",
                     url: "https://bluwm.jp/",
                     exp: "ウェディングペーパーアイテムLINEbotサービス用ランディングページです。"
                },
                {
                    title: "Bluwm LINEbotサービス",
                     image: "/linebot-img.webp",
                     lazy: "/linebot-lazy.webp",
                     skill: "Python/ Django/ heroku",
                     url: "https://line.me/R/ti/p/%40336bwogm",
                     exp: "紙で準備することが当たり前となっている結婚式で用いる招待状をはじめとするペーパーアイテムをLINEbotにしたサービスです。手軽さとコストダウンを叶えます。"
                },
                {
                    title: "Portfolioサイト",
                     image: "/portfolio-img.webp",
                     lazy: "/portfolio-lazy.webp",
                     skill: "Vue.js/ Nuxt.js/ adobe XD/ Netlify",
                     url: "/",
                     exp: "本サイトです。柔らかい色合いでシンプルなデザインを心がけて作成しました。"
                }
            ]
        }
    },
    methods: {
        openDialog(item) {
            this.currentWork = item
            this.dialog = true
        }
    }
}
</script>