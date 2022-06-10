<template>
    <main class="mt-8">
        <v-container>
            <h1 class="mb-4">Projects</h1>

            <v-row>
                <v-col v-for="project in projects" :key="project.id" cols="12" sm="12" md="6" lg="4">
                    <v-card class="mx-auto" max-width="400">
                        <v-sheet class="white--text align-end" :id="project.imgID" height="200px"></v-sheet>

                        <v-card-title>{{ project.title }}</v-card-title>

                        <v-card-subtitle class="pb-0">
                            Project {{ project.id }}
                        </v-card-subtitle>

                        <v-card-text class="text--primary">
                            {{ project.body }}
                        </v-card-text>

                        <v-card-actions>
                            <a :href="project.link.live" target="_blank">
                                <v-btn color="blue" text>View</v-btn>
                            </a>

                            <a :href="project.link.github" target="_blank">
                                <v-btn color="blue" text>Github</v-btn>
                            </a>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>

            <p class="title text-center my-4">
                <NuxtLink class="decorate" to="/projects">View All Projects</NuxtLink>
            </p>
        </v-container>
    </main>
</template>

<script>
export default {
    name: "ProjectsArea",
    data() {
        return {
            projects: [
                {
                    id: "01",
                    imgID: "todoListApp",
                    title: "Todo List App",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://todotrackster.netlify.app/",
                        github: "https://github.com/digvijay-webdev"
                    }
                },
                {
                    id: "02",
                    imgID: "moq",
                    title: "Multiverse of Question",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://multiverseofquestion.com/",
                        github: "https://github.com/digvijay-webdev"
                    }
                },
                {
                    id: "03",
                    imgID: "baseluck",
                    title: "Shree Bhavani Sound Co.",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://base-luck.netlify.app/",
                        github: "https://github.com/digvijay-webdev"
                    }
                }
            ]
        }
    }
}
</script>

<style scoped>
main {
    background-color: #ecf0f1;
}

#todoListApp {
    background: url("../../static/images/todo-list-app.jpg") no-repeat;
    background-position: center;
    background-size: cover;
}

#moq {
    background: url("../../static/images/moq-home.png") no-repeat;
    background-position: center;
    background-size: cover;
}

#baseluck {
    background: url("../../static/images/baseluck.png") no-repeat;
    background-position: center;
    background-size: cover;
}

a {
    text-decoration: none;
}

.decorate:hover {
    text-decoration: underline;
}
</style>
