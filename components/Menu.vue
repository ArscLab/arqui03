<template>
    <v-app-bar color="blue-darken-3" density="compact">
        <template v-slot:prepend>
            <v-btn icon="mdi-filmstrip"></v-btn>
        </template>

        <v-app-bar-title>Movies</v-app-bar-title>

        <template v-slot:append>
            <v-btn icon="mdi-exit-to-app"></v-btn>
        </template>
    </v-app-bar>


</template>