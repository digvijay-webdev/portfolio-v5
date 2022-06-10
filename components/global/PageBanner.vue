<template>
    <div class="banner">
        <div class="overlay">
            <v-container>
                <h1 class="display-1 text-center white--text">
                    {{ pageTitle }}
                </h1>
            </v-container>
        </div>
    </div>
</template>

<script>
export default {
    name: "PageBanner",
    props: ["pageTitle"]
}
</script>

<style scoped>
.banner {
    height: 250px;
    background: url("../../static/images/bg-1-medium.jpg") no-repeat;
    background-position: center;
    background-size: cover;
    position: relative;
}

.banner .overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: #0000008f;
    display: flex;
    justify-content: center;
    align-items: center;
}
</style>
