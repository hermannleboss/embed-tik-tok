<template>
    <div>
        <h1>Try the API from tiktok doc</h1>
        <h2>Creator page</h2>
        <ClientOnly fallback-tag="span" fallback="Loading tiktok creator page">
            <blockquote class="tiktok-embed" cite="https://www.tiktok.com/@sami.et09" data-unique-id="sami.et09"
                data-embed-type="creator" style="max-width: 780px; min-width: 288px">
                <section>
                    <a target="_blank" href="https://www.tiktok.com/@sami.et09?refer=creator_embed">@sami.et09</a>
                </section>
            </blockquote>
        </ClientOnly>

        <h2>Fetch from api</h2>
        <div>
            <div v-if="pending">Loading...</div>
            <div v-if="error">Error : {{ error.message }}</div>
            <div v-if="data">
                <h3>Embedded script</h3>
                <div v-html="removeScriptTag(data.html)"></div>
                <h3>Fetch Data</h3>
                <div style="overflow: auto;">                    
                <pre>{{ data }}</pre>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

const { data, pending, error, refresh } = useFetch(
    "https://www.tiktok.com/oembed?url=https://www.tiktok.com/@dineiro.off/video/7333638669569428768"
);

const removeScriptTag = (html: string) => {
    return html.replace(/<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>/gi, '');
}
</script>

<style scoped></style>
