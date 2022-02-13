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
        v-for="item in items"
        :key="item.title"
        class="ma-5"
        >
            <v-img
            :src= "item.image"
            >
            </v-img>

                    <v-card-title>
            {{ item.title }}
        </v-card-title>

            <v-card-text>
                {{ item.skill }}
            </v-card-text>
        </v-card>
    </div>

        </v-col>
    </v-row>
</template>

<script>
export default {
    data() {
        return {
            items: [
                {
                    title: "オンラインペーパーアイテム",
                     image: "/sample.jpg",
                     skill: "skillsetskillsetskillset",
                     url: "https://bluwm.jp/"
                },
                {
                    title: "オンラインペーパーアイテム",
                     image: "/sample.jpg",
                     skill: "skillsetskillsetskillset2",
                     url: "https://bluwm.jp/"
                },
                {
                    title: "オンラインペーパーアイテム",
                     image: "/sample.jpg",
                     skill: "skillsetskillsetskillset3",
                     url: "https://bluwm.jp/"
                }
            ]
        }
    }
}
</script>