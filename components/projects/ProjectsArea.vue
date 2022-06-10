<template>
    <main>
        <v-container class="my-6">
            <v-row>
                <v-col v-for="project in projects" :key="project.id" cols="12" sm="12" md="6" lg="4">
                    <v-card class="mx-auto card" max-width="400" elevation="2">
                        <v-sheet :id="project.imgID" class="white--text align-end"  height="200px"></v-sheet>

                        <v-card-title>
                            {{ project.title }}
                        </v-card-title>

                        <v-card-subtitle class="pb-0">
                            Awesome project
                        </v-card-subtitle>

                        <v-card-text class="text--primary">
                            {{ project.body }}

                            <p class="pt-2">
                                <span class="subtitle">Tech Keywords:</span><br>
                                <span>
                                    {{ project.lang }}
                                </span>
                            </p>
                            <v-chip v-if="!project.link.live" color="warning white--text" pill>In progress</v-chip>
                        </v-card-text>

                        <v-card-actions>
                            <a :href="project.link.live" target="_blank">
                                <v-btn color="blue" :disabled="!project.link.live" text>View</v-btn>
                            </a>

                            <a :href="project.link.github" target="_blank">
                                <v-btn color="blue" text>Github</v-btn>
                            </a>
                        </v-card-actions>
                    </v-card>
                </v-col>
            </v-row>
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
                    lang: "Vue, Nuxt, PWA",
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
                    lang: "Vue, Vuex, REST API, Node.js, Express, MongoDB, Atlas, Heroku",
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
                    lang: "HTML5, CSS3, Vue, Nuxt, Node.js, Express, MongoDB",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://base-luck.netlify.app/",
                        github: "https://github.com/digvijay-webdev"
                    }
                },
                {
                    id: "04",
                    imgID: "appleUIClone",
                    title: "Apple Home Page UI Clone",
                    lang: "HTML5, CSS3, JavaScript, Bootstrap4",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://apple-ui-clone.netlify.app/",
                        github: "https://github.com/digvijay-webdev"
                    }
                },
                {
                    id: "05",
                    imgID: "qrCodeGen",
                    title: "QR Code Generator",
                    lang: "Node.js, Express, REST API, MaterialiseCSS",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        live: "https://digvijay-qrgen.herokuapp.com/",
                        github: "https://github.com/digvijay-webdev"
                    }
                },
                {
                    id: "06",
                    imgID: "whatsAppClone",
                    title: "What's App UI Clone",
                    lang: "Flutter, Dart, Native Mobile Application",
                    body: "Lorem ipsum dolor sit amet consectetur adipisicing elit. Soluta laborum eveniet illum dolorem! Eum maxime nesciunt repellendus mollitia, iste id aperiam esse dolore inventore animi ex error impedit.",
                    link: {
                        github: "https://github.com/digvijay-webdev"
                    }
                }
            ]
        }
    }
}
</script>

<style scoped>

a {
    text-decoration: none;
}

/* Backgrounds */
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

#appleUIClone {
    background: url("../../static/images/apple-ui-clone.png") no-repeat;
    background-position: center;
    background-size: cover;
}

#qrCodeGen {
    background: url("../../static/images/qr-gen.png") no-repeat;
    background-position: center;
    background-size: cover;
}

#whatsAppClone {
    background: url("../../static/images/placeholder-image.png") no-repeat;
    background-position: center;
    background-size: cover;
}

</style>
