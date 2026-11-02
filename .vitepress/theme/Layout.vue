<script setup lang="ts">
import DefaultTheme from 'vitepress/theme'
import HostingBadge from './components/HostingBadge.vue'
import SponsorBanner from './SponsorBanner.vue'
import SponsorSlots from './SponsorSlots.vue'

const { Layout } = DefaultTheme
</script>

<template>
    <Layout>
        <template #home-hero-before>
            <SponsorBanner />
        </template>
        <template #doc-before>
            <SponsorBanner />
        </template>
        <template #aside-outline-after>
            <SponsorSlots :count="1" />
        </template>
        <template #layout-bottom>
            <div class="vp-footer-hosting">
                <HostingBadge />
            </div>
        </template>
    </Layout>
</template>

<style>
.vp-footer-hosting {
    display: flex;
    justify-content: center;
    padding: 12px 24px 24px;
    color: var(--vp-c-text-2);
    font-size: 13px;
}
</style>
