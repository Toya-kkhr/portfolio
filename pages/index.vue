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
  mounted() {
    const about = this.$scrollmagic
    .scene({
      triggerElement: '#about' ,
      triggerHook: 0,
      offset: -600,
      duration: 300,
      reverse: true
    })
    .setTween('#about',{
      css: {
        opacity: '1'
      }
    })

    this.$scrollmagic.addScene(about)
    
    const skills = this.$scrollmagic
    .scene({
      triggerElement: '#skills' ,
      triggerHook: 0,
      offset: -500,
      duration: 400,
      reverse: true
    })
    .setTween('#skills',{
      css: {
        opacity: '1'
      }
    })

    this.$scrollmagic.addScene(skills)

    const works = this.$scrollmagic
    .scene({
      triggerElement: '#works' ,
      triggerHook: 0,
       offset: -500,
      duration: 600,
      reverse: true
    })
    .setTween('#works',{
      css: {
        opacity: '1'
      }
    })

    this.$scrollmagic.addScene(works)

    const hobbys = this.$scrollmagic
    .scene({
      triggerElement: '#hobbys' ,
      triggerHook: 0,
      offset: -500,
      duration: 500,
      reverse: true
    })
    .setTween('#hobbys',{
      css: {
        opacity: '1'
      }
    })

    this.$scrollmagic.addScene(hobbys)

    const contact = this.$scrollmagic
    .scene({
      triggerElement: '#contact' ,
      triggerHook: 0,
      offset: -400,
      duration: 300,
      reverse: true
    })
    .setTween('#contact',{
      css: {
        opacity: '1'
      }
    })

    this.$scrollmagic.addScene(contact)

  }


}
</script>
