


<template>


    <v-card>
        <v-toolbar>
            <div class="headline"> Add A Note </div>
        </v-toolbar>
        <v-container fluid>
            <v-card-text>

                <!-- Begin Input Row -->
                <v-form ref="form">
                    <v-text-field label="Title" v-model="note.title"> </v-text-field>

                    <v-text-field label="Content" v-model="note.content" multi-line> </v-text-field>

                    <v-btn @click="$emit('submission', note); note={}" class="green lighten-1 white--text">Submit</v-btn>
                    <v-btn @click="$emit('closeAdd')" class="red white--text">Close</v-btn>
                </v-form>
            </v-card-text>
        </v-container>
    </v-card>

</template>

<script>
    export default {
        data: () => ({
            note: {
                title: '',
                content: ''

            }
        }),

        props: {
            rules: {
                type: Object
            }
        }
    }
</script>
