<template>
    <v-app-bar app color="black" dark flat class="px-12">
        <v-btn>
            <v-icon color="yellow" left class="mr-2">fas fa-signature</v-icon> Amare
        </v-btn>

        <v-spacer></v-spacer>

        <!-- Desktop Navigation -->
        <div class="d-none d-md-flex">
            <v-btn text @click="scroll('home')" class="text-yellow">Home</v-btn>
            <v-btn text @click="scroll('about')">About</v-btn>
            <v-btn text @click="scroll('portfolio')">Portfolio</v-btn>
            <v-btn text @click="scroll('services')"> Services</v-btn>
            <v-btn text @click="scroll('page')"> Page</v-btn>
            <v-btn text @click="scroll('biog')"> Biog</v-btn>
            <v-btn text @click="scroll('contact')"> Contact</v-btn>
        </div>

        <!-- Mobile Navigation -->
        <v-app-bar-nav-icon @click="drawer = !drawer" class="d-md-none"></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer
        v-model="drawer"
        app
        temporary
        class="d-md-none"
    >
        <v-list dense>
            <v-list-item @click="scroll('home')">
                <v-list-item-title>Home</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('about')">
                <v-list-item-title>About</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('portfolio')">
                <v-list-item-title>Portfolio</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('services')">
                <v-list-item-title>Services</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('page')">
                <v-list-item-title>Page</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('biog')">
                <v-list-item-title>Biog</v-list-item-title>
            </v-list-item>
            <v-list-item @click="scroll('contact')">
                <v-list-item-title>Contact</v-list-item-title>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>
</template>

<script>
export default {
    data() {
        return {
            drawer: false,
        };
    },
    methods: {
        scroll(refName) {
            const element = document.getElementById(refName);
            element.scrollIntoView({ behavior: "smooth" });
            this.drawer = false;  // Close the drawer after clicking a link
        },
    },
};
</script>

<style>
/* Adjust padding for mobile view */
@media (max-width: 960px) {
    .px-12 {
        padding-left: 16px !important;
        padding-right: 16px !important;
    }
}
</style>
