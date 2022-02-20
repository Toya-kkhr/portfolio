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
                :repeat="Infinity"
                :type-delay="90"
                :pre-type-delay="1000"
                :erase-delay="110"
                :pre-erase-delay="2000"
                caret-animation="smooth"
                erase-style="backspace"
                initial-action="typing"
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
