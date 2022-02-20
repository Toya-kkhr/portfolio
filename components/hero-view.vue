<template>
      <v-parallax
      src="/background.png"
      align="center"
      >
        <v-container
        class="text-center"
        >
             <h1
             style="font-weight: 300;"
             >
                <vue-typer
                :text="hero"
                :repeat="0"
                :type-delay="80"
                caret-animation="smooth"
                ></vue-typer>
          
        </h1>
        </v-container>
      </v-parallax>
</template>

<script>
export default {
           name: "TopPage",
    data() {
        return {
            hero: "TOYA KAKOHARA\n Portfolio"
        }
    }
}
</script>
