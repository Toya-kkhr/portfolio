<template>
       <v-row
    align="center"
    justify="center"
    >
      <v-col
      cols="12"
      sm="6"
      align="center"
      >
        <div
        class="pa-3"
        >
    <h2
      style="text-decoration: underline;"
    >
      About
      </h2>
    </div>
    <div
    class="pa-3"
    >
      <v-img
      src="/profile.webp"
      lazy-src="/profile-lazy.webp"
      width="199px"
      height="207px"
      style="border-radius: 50%;"
      >
      </v-img>
    </div>
    <div class="pa-2">加古原 冬弥</div>
    <div
    class="ma-3 text-body-1"
    >
 大阪生まれ24歳。専門学校卒業後、某ホテルにて3年弱ウェディングプランナーとして従事。
 その後独学でプログラミングを学び、受託開発会社にてプログラマーを経験後、現在自社サービス開発会社にて上流工程に携わっている。
    </div>
    <div>
      <v-btn
        width="60%"
        height="50px"
        class="rounded-pill"
        href="https://blog.kakohara.me/"
        target="_blank"
      >
        BLOGサイトへ
      </v-btn>
    </div>
          </v-col>
    </v-row>
</template>

<script>
export default {
  name: "AboutPage"
}
</script>