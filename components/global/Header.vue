<template>
    <header>
        <v-app-bar color="deep-purple" dark>
            <v-container class="adjustAlignment">
                <v-toolbar-title>
                    <NuxtLink to="/" class="brand">d:/></NuxtLink>
                </v-toolbar-title>

                <div class="links">
                    <NuxtLink to="/">Home</NuxtLink>
                    <NuxtLink to="/blog">Blog</NuxtLink>
                    <NuxtLink to="/projects">Projects</NuxtLink>
                    <a href="mailto:djpadhiyar881@gmail.com">Contact</a>
                </div>

                <v-app-bar-nav-icon @click="drawer = true" class="toggler"></v-app-bar-nav-icon>
            </v-container>
        </v-app-bar>

        <!-- drawer for small screens -->
        <v-navigation-drawer v-model="drawer" absolute temporary>
            <v-list nav dense>
                <v-list-item-group v-model="group" active-class="deep-purple--text text--accent-4">
                    <NuxtLink to="/">
                        <v-list-item>
                            <v-list-item-icon>
                                <v-icon>mdi-home</v-icon>
                            </v-list-item-icon>
                            <v-list-item-title>Home</v-list-item-title>
                        </v-list-item>
                    </NuxtLink>
                    <NuxtLink to="/blog">
                        <v-list-item>
                            <v-list-item-icon>
                                <v-icon>mdi-post</v-icon>
                            </v-list-item-icon>
                            <v-list-item-title>Blog</v-list-item-title>
                        </v-list-item>
                    </NuxtLink>
                    <NuxtLink to="/projects">
                        <v-list-item>
                            <v-list-item-icon>
                                <v-icon>mdi-rocket-launch</v-icon>
                            </v-list-item-icon>
                            <v-list-item-title>Projects</v-list-item-title>
                        </v-list-item>
                    </NuxtLink>
                    <a href="mailto:djpadhiyar881@gmail.com">
                        <v-list-item>
                            <v-list-item-icon>
                                <v-icon>mdi-email</v-icon>
                            </v-list-item-icon>
                            <v-list-item-title>Get in touch</v-list-item-title>
                        </v-list-item>
                    </a>
                </v-list-item-group>
            </v-list>
        </v-navigation-drawer>
    </header>
</template>

<script>
export default {
    name: "Header",
    data() {
        return {
            drawer: false,
            group: null
        }
    }
}
</script>

<style scoped>
.adjustAlignment {
    display: flex;
    align-items: center;
    justify-content: space-between;
}

a {
    text-decoration: none;
}

.brand {
    color: #fff;
    font-weight: bold;
}

.links a {
    color: #fff;
    margin-left: 8px;
    transition: all .3s ease;
}

.links a:hover {
    font-weight: bold;
}

.nuxt-link-exact-active {
    font-weight: bold;
}

.toggler {
    display: none;
}

/* Media Query */
@media screen and (max-width: 720px) {
    .toggler {
        display: block;
    }
    .links {
        display: none;
    }
}
</style>
