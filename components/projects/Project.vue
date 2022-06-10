<template>
    <section>
        <!-- :id="project.imgID" -->
        <v-card class="mx-auto card" max-width="400" elevation="0">
            <v-sheet :imageID="imgID" class="white--text align-end"  height="200px"></v-sheet>

            <v-card-title>{{ title }}</v-card-title>

            <v-card-subtitle class="pb-0">
                Awesome project
            </v-card-subtitle>

            <v-card-text class="text--primary">
                {{ body }}
            </v-card-text>

            <v-card-actions>
                <a :href="preview" target="_blank">
                    <v-btn color="blue" text>View</v-btn>
                </a>

                <a :href="github" target="_blank">
                    <v-btn color="blue" text>Github</v-btn>
                </a>
            </v-card-actions>
        </v-card>
    </section>
</template>

<script>
export default {
    name: "Project",
    props: ["title", "body", "preview", "github", "imgID"]
}
</script>

<style scoped>
a {
    text-decoration: none;
}

.card {
    border: 1px solid #3333335d;
}

</style>
