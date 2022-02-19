<template>
      <v-parallax
      src="/background.png"
      align="center"
      >
        <v-container
        class="text-center"
        >
             <h1
             class="text-h2"
             >
                <vue-typer
                :text="hero"
                :repeat="0"
                :type-delay="150"
                :caret-animation="smooth"
                ></vue-typer>
          
        </h1>
        </v-container>
      </v-parallax>
</template>

<script>
export default {
    data() {
        return {
            hero: "TOYA\n KAKOHARA\n Portfolio"
        }
    }
}
</script>
