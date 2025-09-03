<script setup lang="ts">
import FeaturesWidget from '@/components/landing/FeaturesWidget.vue';
import FooterWidget from '@/components/landing/FooterWidget.vue';
import HeroWidget from '@/components/landing/HeroWidget.vue';
import HighlightsWidget from '@/components/landing/HighlightsWidget.vue';
import PricingWidget from '@/components/landing/PricingWidget.vue';
import TopbarWidget from '@/components/landing/TopbarWidget.vue';
</script>

<template>
    <div class="bg-surface-0 dark:bg-surface-900">
        <div id="home" class="landing-wrapper overflow-hidden">
            <div class="py-6 px-6 flex items-center justify-between fixed top-0 left-0 right-0 z-50 bg-black text-white w-full">
                <TopbarWidget />
            </div>
            <div class="h-24"></div>
            <HeroWidget />
            <FeaturesWidget />
            <PricingWidget />
            <HighlightsWidget />
            <FooterWidget />
        </div>
    </div>
</template>
