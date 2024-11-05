<template>
    <v-bottom-navigation v-model="active" active mode="shift" absolute>
        <v-btn value="ship">
            <Icon icon="fluent:vehicle-ship-24-filled" class="w-6 h-6" />
            <span>航次</span>
        </v-btn>

        <v-btn value="purse">
            <Icon icon="lsicon:purse-outline" class="w-6 h-6" />
            <span>收支</span>
        </v-btn>
    </v-bottom-navigation>
</template>

<script setup>
import { Icon } from '@iconify/vue';
import { onMounted, ref, watch } from 'vue';
import { useRouter } from 'vue-router';

const router = useRouter();

const active = ref('ship');

watch(active, (newValue) => {
    if (newValue) {
        router.push(newValue).catch((err) => console.error('跳转错误:', err));
    }
});

onMounted(() => {
    router.push(active.value).catch((err) => console.error('初始化跳转错误:', err));
});
</script>

<style lang="scss" scoped></style>