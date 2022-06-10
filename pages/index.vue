<template>
  <main>
    <LandingArea />
    <AboutMe />
    <ProjectsArea />
  </main>
</template>

<script>
import LandingArea from "../components/home/LandingArea.vue"
import AboutMe from "../components/home/AboutMe.vue"
import ProjectsArea from "../components/home/ProjectsArea.vue"

export default {
  name: "HomePage",
  components: {
    LandingArea,
    AboutMe,
    ProjectsArea
  }
}
</script>

<style scoped>

</style>
