<template>
    <main class="mt-8">
        <v-container>
            <h1 class="">About me</h1>

            <v-row>
                <v-col cols="12" sm="12" md="12" lg="6">
                    <p class="title">Hi, I'm Digvijay</p>
                    <p class="body">
                        A passionate self-taught developer who likes to code and learn new things. I enjoy making beautiful UI and amazing Back-Ends with node.js
                    </p>
                    <p class="body">
                        An international student from India pursuing bachelor's of Computer Science at the University of East London. I've been programming since last 5 years. Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aperiam reprehenderit praesentium exercitationem modi eos, assumenda cum molestiae ullam. Quae voluptatum qui dolorum! Atque ab eveniet quia, assumenda omnis culpa eligendi aut consectetur incidunt eaque quod dolor alias ducimus veritatis maiores vero magnam quo ratione ipsum.
                    </p>

                    <h3>Top Expertise</h3>
                    <v-row>
                        <v-col cols="12" sm="12" md="6" lg="6">
                            <ul>
                                <li>JavaScript</li>
                                <li>Vue.js</li>
                                <li>Nuxt</li>
                                <li>Node/Express</li>
                            </ul>
                        </v-col>
                        <v-col cols="12" sm="12" md="6" lg="6">
                            <ul>
                                <li>Flutter/Dart</li>
                                <li>MongoDB</li>
                                <li>Heroku</li>
                                <li>Python</li>
                            </ul>
                        </v-col>
                    </v-row>
                </v-col>

                <v-col cols="12" sm="12" md="12" lg="6">
                    <v-carousel cycle hide-delimiter-background show-arrows-on-hover height="300">
                        <v-carousel-item>
                            <img src="../../static/images/cert-1.png" height="100%" width="100%" aspect-ratio="1.7" />
                        </v-carousel-item>
                        <v-carousel-item>
                            <img src="../../static/images/cert-2.png" height="100%" width="100%" aspect-ratio="1.7" />
                        </v-carousel-item>
                    </v-carousel>
                </v-col>
            </v-row>
        </v-container>
    </main>
</template>

<script>
export default {
    name: "AboutMe"
}
</script>

<style scoped>

</style>
