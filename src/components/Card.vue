<template>
    <v-flex xs12 sm6 md4>
        <v-card>
            <v-img
                    :src="require(image)"
                    height="200px"
            >
            </v-img>

            <v-card-title primary-title>
                <div>
                    <slot name="title"></slot>
                    <slot name="subtitle"></slot>
                </div>
            </v-card-title>

            <v-card-text>
                <slot name="content"></slot>
            </v-card-text>

            <v-card-actions>
                <v-btn flat>Share</v-btn>
                <v-btn flat color="purple">Explore</v-btn>
                <v-spacer></v-spacer>
                <v-btn icon @click="show = !show">
                    <v-icon>{{ show ? 'keyboard_arrow_down' : 'keyboard_arrow_up' }}</v-icon>
                </v-btn>
            </v-card-actions>

            <v-slide-y-transition>
                <v-card-text v-show="show">
                    I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have
                    time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that
                    data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry?
                    I've got to find a way to escape.
                </v-card-text>
            </v-slide-y-transition>
        </v-card>
    </v-flex>
</template>

<script>
    export default {
        name: "Card",
        props: {
            title: String,
            subtitle: String,
            image: String,
            content: String,
            dropdownContent: String
        }
    };
</script>

<style scoped>
</style>