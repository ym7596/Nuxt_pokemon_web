<template>
    <v-card
    class="mx-auto"
    max-width="300"
    max-height="380">
    <v-img
    :src="data.imgsrc"
    alt = "Image"
    height="auto"
    ></v-img>
    <v-card-title>
        <span>{{ data.Name_ko }} ({{ data.Name }})</span>
    </v-card-title>
    <v-card-subtitle>
        <span>{{ data.Type1 }}</span>
        <span v-if="data.Type2 != 'None'">/ {{ data.Type2 }}</span>
    </v-card-subtitle>
    </v-card>
</template>
<script>
export default {
    props: {
        data: {
            type: Object,
            required: true
        }
    },
    
}
</script>
<style>
    
</style>