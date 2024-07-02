<template>
    <v-footer>
        <v-card elevation="0" rounded="0" width="100%" class="bg-grey text-center">
            <v-card-text>
                <v-row justify="center">
                    <v-col cols="4" sm="auto">
                        <v-btn class="mx-2" icon href="https://telegram.me/A12arts" target="_blank" color="white">
                            <v-icon>fab fa-telegram</v-icon>
                        </v-btn>
                    </v-col>
                    <v-col cols="4" sm="auto">
                        <v-btn class="mx-2" icon href="https://www.instagram.com/amare_arts4" target="_blank" color="white">
                            <v-icon>fab fa-instagram</v-icon>
                        </v-btn>
                    </v-col>
                    <v-col cols="4" sm="auto">
                        <v-btn class="mx-2" icon href="https://www.facebook.com/" target="_blank" color="white">
                            <v-icon>fab fa-facebook</v-icon>
                        </v-btn>
                    </v-col>
                </v-row>
            </v-card-text>

            <v-card-text class="text-white">
                @ {{ new Date().getFullYear() }} —
                <strong>AbrshXo9 All Rights Reserved</strong>
            </v-card-text>
        </v-card>
    </v-footer>
</template>

<script>
export default {

}
</script>

<style>
.v-footer {
    padding: 8px 0 !important;
}
@media (max-width: 600px) {
    .v-btn {
        margin: 0 4px !important;
    }
}
</style>
