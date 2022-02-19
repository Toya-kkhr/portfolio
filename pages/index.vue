<template>
<div>

<hero-view />

  <div
  id="about"
  class="mb-5"
  >
  <v-container
  class="my-12"
  >
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
      style="background: #E0E1DB;"
       class="mb-5"
>
    <v-container>
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
</div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
