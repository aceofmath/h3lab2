<script setup lang="ts">
import ContactWidget from '@/components/landing/ContactWidget.vue';
import FooterWidget from '@/components/landing/FooterWidget.vue';
import MainWidget from '@/components/landing/MainWidget.vue';
import PortfolioWidget from '@/components/landing/PortfolioWidget.vue';
import ServiceWidget from '@/components/landing/ServiceWidget.vue';
import TopbarWidget from '@/components/landing/TopbarWidget.vue';
</script>

<template>
    <div class="bg-surface-0 dark:bg-surface-900">
        <div id="home" class="landing-wrapper overflow-hidden">
            <div class="py-6 px-6 flex items-center justify-between fixed top-0 left-0 right-0 z-50 bg-black text-white w-full">
                <TopbarWidget />
            </div>
            <div class="h-24"></div>
            <MainWidget />
            <ServiceWidget />
            <PortfolioWidget />
            <ContactWidget />
            <FooterWidget />
        </div>
    </div>
</template>
