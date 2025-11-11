<script setup lang="ts">
    import MainSidebar from '@/components/ui/Custom/MainSidebar.vue';
import SidebarProvider from '@/components/ui/sidebar/SidebarProvider.vue';
    import { Head } from '@inertiajs/vue3';

    defineProps<{
        title: string
    }>();
</script>

<template>
    <Head :title="title"  />
    <SidebarProvider>
        <MainSidebar />
        <main>
            <slot />
        </main>
    </SidebarProvider>
</template>
