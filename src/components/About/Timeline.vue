<template>
    <div class="timeline">
        <div v-for="e in education" :key="e.Year">
            <div class="text">
                <div class="year">{{ e.Year }}</div>
                <div class="institute">{{ e.InstituteName }}</div>
                <div class="program">{{ e.Program }}</div>
            </div>
        </div>
    </div>
</template>

<script lang="ts">
export default {
    name: "Timeline",
    props: ["education"],
};
</script>

<style lang="scss" scoped>
@import "../../scss/components/timeline";
</style>
