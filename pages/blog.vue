<template>
    <main>
        <PageHeader pageTitle="Blogs" />
        <v-container class="spacer">
            <h1 class="text-center">No blogs published yet..</h1>
        </v-container>
    </main>
</template>

<script>
import PageHeader from "../components/global/PageBanner.vue"

export default {
    name: "blog",
    components: {
        PageHeader
    }
}
</script>

<style scoped>
.spacer {
    height: 80vh;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
