<template>
    <main>
        <LandingArea />
        <ProjectsArea />
    </main>
</template>

<script>
import LandingArea from "../components/projects/LandingArea.vue"
import ProjectsArea from "../components/projects/ProjectsArea.vue"

export default {
    name: "Projects",
    components: {
        LandingArea,
        ProjectsArea
    }
}
</script>

<style scoped>

</style>
