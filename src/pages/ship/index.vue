<template>
    <v-row dense class="!m-3 gap-4">
        <v-col v-for="index in 10" :key="index" class="p-2" cols="12">
            <v-card>
                <v-card-title class="text-h5">
                    Unlimited music now
                </v-card-title>

                <v-card-subtitle>
                    Listen to your favorite artists and albums whenever and wherever, online and offline.
                </v-card-subtitle>

                <v-card-actions>
                    <v-btn text="Listen Now" variant="text"></v-btn>
                </v-card-actions>
            </v-card>
        </v-col>
    </v-row>
</template>

<script setup>

</script>

<style lang="scss" scoped>
/* 这里可以添加一些自定义样式 */
</style>