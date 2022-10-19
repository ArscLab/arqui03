<template>
    <v-app>
        <v-sheet class="mx-auto" elevation="5" max-width="100%" width="100%">
            <v-slide-group v-model="model" class="pa-8" selected-class="bg-success" 
            
            show-arrows>
                <v-slide-group-item v-for="(item,i) in items" :key="i" v-slot="{ toggle }">
                    <v-card color="grey-lighten-3" elevation="6" class="ma-3" height="600" width="500"
                        @click="toggle">
                        <h3>{{item.title}}</h3>
                        <v-card-text>
                            {{item.description}}
                        </v-card-text>
                        <h4> Director</h4>
                        <h5> {{item.director}}</h5>
                        <v-img aspect-ratio="1" width="80%" src="http://agroworldspain.com/img/noimage.png" ></v-img>
                        <!--<v-img aspect-ratio="1" width="100%" :src="item.src" ></v-img>

                        <v-card-actions  class="pa-1">
                            <NuxtLink tag="li" to="/about" class="pa-1">
                                <v-btn variant="outlined" class="bg-blue-darken-2">
                                    Ver autor
                                </v-btn>
                            </NuxtLink>
                            <NuxtLink to="/about" class="pa-1">
                                <v-btn variant="outlined" class="bg-blue-darken-2">
                                    Ver director
                                </v-btn>
                            </NuxtLink>
                        </v-card-actions>
                        -->
                    </v-card>
                </v-slide-group-item>
            </v-slide-group>
        </v-sheet>
    </v-app>
</template>

<style>
a{
    text-decoration: none;
}
</style>

<script setup>

const { items } = await import('~/content/movies.json')
console.log(items);
</script>