<script setup lang="ts">
type GapSizes =
    "0"
    | "px"
    | "0.5"
    | "1"
    | "1.5"
    | "2"
    | "2.5"
    | "3"
    | "3.5"
    | "4"
    | "5"
    | "6"
    | "7"
    | "8"
    | "9"
    | "10"
    | "11"
    | "12";

const props = defineProps<{
    row?: boolean;
    smRow?: boolean;
    mdRow?: boolean;
    lgRow?: boolean;
    xlRow?: boolean;
    txlRow?: boolean;
    column?: boolean;
    smColumn?: boolean;
    mdColumn?: boolean;
    lgColumn?: boolean;
    xlColumn?: boolean;
    txlColumn?: boolean;
    wrap?: boolean;
    grow?: boolean;
    noGrow?: boolean;
    shrink?: boolean;
    noShrink?: boolean;
    router?: boolean;
    to?: string;
    is?: string;
    items?: "start" | "center" | "end";
    smItems?: "start" | "center" | "end";
    mdItems?: "start" | "center" | "end";
    lgItems?: "start" | "center" | "end";
    xlItems?: "start" | "center" | "end";
    txlItems?: "start" | "center" | "end";
    justify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    smJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    mdJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    lgJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    xlJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    txlJustify?: "start" | "center" | "end" | "between" | "around" | "evenly";
    gap?: GapSizes,
    gapX?: GapSizes,
    gapY?: GapSizes,
}>();
</script>

<template>
    <NuxtLink v-if="router" :to="to" class="flex"
              :class="{'flex-row': props.row, 'sm:flex-row': props.smRow, 'md:flex-row': props.mdRow, 'lg:flex-row': props.lgRow, 'xl:flex-row': props.xlRow, '2xl:flex-row': props.txlRow, 'flex-col': props.column, 'sm:flex-col': props.smColumn, 'md:flex-col': props.mdColumn, 'lg:flex-col': props.lgColumn, 'xl:flex-col': props.xlColumn, '2xl:flex-col': props.txlColumn, 'flex-wrap': props.wrap, 'justify-start': props.justify === 'start', 'justify-center': props.justify === 'center', 'justify-end': props.justify === 'end', 'justify-between': props.justify === 'between', 'justify-around': props.justify === 'around', 'justify-evenly': props.justify === 'evenly', 'sm:justify-start': props.smJustify === 'start', 'sm:justify-center': props.smJustify === 'center', 'sm:justify-end': props.smJustify === 'end', 'sm:justify-between': props.smJustify === 'between', 'sm:justify-around': props.smJustify === 'around', 'sm:justify-evenly': props.smJustify === 'evenly', 'md:justify-start': props.mdJustify === 'start', 'md:justify-center': props.mdJustify === 'center', 'md:justify-end': props.mdJustify === 'end', 'md:justify-between': props.mdJustify === 'between', 'md:justify-around': props.mdJustify === 'around', 'md:justify-evenly': props.mdJustify === 'evenly', 'lg:justify-start': props.lgJustify === 'start', 'lg:justify-center': props.lgJustify === 'center', 'lg:justify-end': props.lgJustify === 'end', 'lg:justify-between': props.lgJustify === 'between', 'lg:justify-around': props.lgJustify === 'around', 'lg:justify-evenly': props.lgJustify === 'evenly', 'xl:justify-start': props.xlJustify === 'start', 'xl:justify-center': props.xlJustify === 'center', 'xl:justify-end': props.xlJustify === 'end', 'xl:justify-between': props.xlJustify === 'between', 'xl:justify-around': props.xlJustify === 'around', 'xl:justify-evenly': props.xlJustify === 'evenly', '2xl:justify-start': props.txlJustify === 'start', '2xl:justify-center': props.txlJustify === 'center', '2xl:justify-end': props.txlJustify === 'end', '2xl:justify-between': props.txlJustify === 'between', '2xl:justify-around': props.txlJustify === 'around', '2xl:justify-evenly': props.txlJustify === 'evenly', 'items-start': props.items === 'start', 'items-center': props.items === 'center', 'items-end': props.items === 'end', 'sm:items-start': props.smItems === 'start', 'sm:items-center': props.smItems === 'center', 'sm:items-end': props.smItems === 'end', 'md:items-start': props.mdItems === 'start', 'md:items-center': props.mdItems === 'center', 'md:items-end': props.mdItems === 'end', 'lg:items-start': props.lgItems === 'start', 'lg:items-center': props.lgItems === 'center', 'lg:items-end': props.lgItems === 'end', 'xl:items-start': props.xlItems === 'start', 'xl:items-center': props.xlItems === 'center', 'xl:items-end': props.xlItems === 'end', '2xl:items-start': props.txlItems === 'start', '2xl:items-center': props.txlItems === 'center', '2xl:items-end': props.txlItems === 'end', 'flex-grow-0': props.noGrow, 'flex-grow': props.grow, 'flex-shrink-0': props.noShrink, 'flex-shrink': props.shrink, 'gap-0': props.gap === '0', 'gap-px': props.gap === 'px', 'gap-0.5': props.gap === '0.5', 'gap-1': props.gap === '1', 'gap-1.5': props.gap === '1.5', 'gap-2': props.gap === '2', 'gap-2.5': props.gap === '2.5', 'gap-3': props.gap === '3', 'gap-3.5': props.gap === '3.5', 'gap-4': props.gap === '4', 'gap-5': props.gap === '5', 'gap-6': props.gap === '6', 'gap-7': props.gap === '7', 'gap-8': props.gap === '8', 'gap-9': props.gap === '9', 'gap-10': props.gap === '10', 'gap-11': props.gap === '11', 'gap-12': props.gap === '12', 'gap-x-0': props.gapX === '0', 'gap-x-px': props.gapX === 'px', 'gap-x-0.5': props.gapX === '0.5', 'gap-x-1': props.gapX === '1', 'gap-x-1.5': props.gapX === '1.5', 'gap-x-2': props.gapX === '2', 'gap-x-2.5': props.gapX === '2.5', 'gap-x-3': props.gapX === '3', 'gap-x-3.5': props.gapX === '3.5', 'gap-x-4': props.gapX === '4', 'gap-x-5': props.gapX === '5', 'gap-x-6': props.gapX === '6', 'gap-x-7': props.gapX === '7', 'gap-x-8': props.gapX === '8', 'gap-x-9': props.gapX === '9', 'gap-x-10': props.gapX === '10', 'gap-x-11': props.gapX === '11', 'gap-x-12': props.gapX === '12', 'gap-y-0': props.gapY === '0', 'gap-y-px': props.gapY === 'px', 'gap-y-0.5': props.gapY === '0.5', 'gap-y-1': props.gapY === '1', 'gap-y-1.5': props.gapY === '1.5', 'gap-y-2': props.gapY === '2', 'gap-y-2.5': props.gapY === '2.5', 'gap-y-3': props.gapY === '3', 'gap-y-3.5': props.gapY === '3.5', 'gap-y-4': props.gapY === '4', 'gap-y-5': props.gapY === '5', 'gap-y-6': props.gapY === '6', 'gap-y-7': props.gapY === '7', 'gap-y-8': props.gapY === '8', 'gap-y-9': props.gapY === '9', 'gap-y-10': props.gapY === '10', 'gap-y-11': props.gapY === '11', 'gap-y-12': props.gapY === '12',}">
        <slot/>
    </NuxtLink>
    <Component :is="is || 'div'" v-else class="flex"
               :class="{'flex-row': props.row, 'sm:flex-row': props.smRow, 'md:flex-row': props.mdRow, 'lg:flex-row': props.lgRow, 'xl:flex-row': props.xlRow, '2xl:flex-row': props.txlRow, 'flex-col': props.column, 'sm:flex-col': props.smColumn, 'md:flex-col': props.mdColumn, 'lg:flex-col': props.lgColumn, 'xl:flex-col': props.xlColumn, '2xl:flex-col': props.txlColumn, 'flex-wrap': props.wrap, 'justify-start': props.justify === 'start', 'justify-center': props.justify === 'center', 'justify-end': props.justify === 'end', 'justify-between': props.justify === 'between', 'justify-around': props.justify === 'around', 'justify-evenly': props.justify === 'evenly', 'sm:justify-start': props.smJustify === 'start', 'sm:justify-center': props.smJustify === 'center', 'sm:justify-end': props.smJustify === 'end', 'sm:justify-between': props.smJustify === 'between', 'sm:justify-around': props.smJustify === 'around', 'sm:justify-evenly': props.smJustify === 'evenly', 'md:justify-start': props.mdJustify === 'start', 'md:justify-center': props.mdJustify === 'center', 'md:justify-end': props.mdJustify === 'end', 'md:justify-between': props.mdJustify === 'between', 'md:justify-around': props.mdJustify === 'around', 'md:justify-evenly': props.mdJustify === 'evenly', 'lg:justify-start': props.lgJustify === 'start', 'lg:justify-center': props.lgJustify === 'center', 'lg:justify-end': props.lgJustify === 'end', 'lg:justify-between': props.lgJustify === 'between', 'lg:justify-around': props.lgJustify === 'around', 'lg:justify-evenly': props.lgJustify === 'evenly', 'xl:justify-start': props.xlJustify === 'start', 'xl:justify-center': props.xlJustify === 'center', 'xl:justify-end': props.xlJustify === 'end', 'xl:justify-between': props.xlJustify === 'between', 'xl:justify-around': props.xlJustify === 'around', 'xl:justify-evenly': props.xlJustify === 'evenly', '2xl:justify-start': props.txlJustify === 'start', '2xl:justify-center': props.txlJustify === 'center', '2xl:justify-end': props.txlJustify === 'end', '2xl:justify-between': props.txlJustify === 'between', '2xl:justify-around': props.txlJustify === 'around', '2xl:justify-evenly': props.txlJustify === 'evenly', 'items-start': props.items === 'start', 'items-center': props.items === 'center', 'items-end': props.items === 'end', 'sm:items-start': props.smItems === 'start', 'sm:items-center': props.smItems === 'center', 'sm:items-end': props.smItems === 'end', 'md:items-start': props.mdItems === 'start', 'md:items-center': props.mdItems === 'center', 'md:items-end': props.mdItems === 'end', 'lg:items-start': props.lgItems === 'start', 'lg:items-center': props.lgItems === 'center', 'lg:items-end': props.lgItems === 'end', 'xl:items-start': props.xlItems === 'start', 'xl:items-center': props.xlItems === 'center', 'xl:items-end': props.xlItems === 'end', '2xl:items-start': props.txlItems === 'start', '2xl:items-center': props.txlItems === 'center', '2xl:items-end': props.txlItems === 'end', 'flex-grow-0': props.noGrow, 'flex-grow': props.grow, 'flex-shrink-0': props.noShrink, 'flex-shrink': props.shrink, 'gap-0': props.gap === '0', 'gap-px': props.gap === 'px', 'gap-0.5': props.gap === '0.5', 'gap-1': props.gap === '1', 'gap-1.5': props.gap === '1.5', 'gap-2': props.gap === '2', 'gap-2.5': props.gap === '2.5', 'gap-3': props.gap === '3', 'gap-3.5': props.gap === '3.5', 'gap-4': props.gap === '4', 'gap-5': props.gap === '5', 'gap-6': props.gap === '6', 'gap-7': props.gap === '7', 'gap-8': props.gap === '8', 'gap-9': props.gap === '9', 'gap-10': props.gap === '10', 'gap-11': props.gap === '11', 'gap-12': props.gap === '12', 'gap-x-0': props.gapX === '0', 'gap-x-px': props.gapX === 'px', 'gap-x-0.5': props.gapX === '0.5', 'gap-x-1': props.gapX === '1', 'gap-x-1.5': props.gapX === '1.5', 'gap-x-2': props.gapX === '2', 'gap-x-2.5': props.gapX === '2.5', 'gap-x-3': props.gapX === '3', 'gap-x-3.5': props.gapX === '3.5', 'gap-x-4': props.gapX === '4', 'gap-x-5': props.gapX === '5', 'gap-x-6': props.gapX === '6', 'gap-x-7': props.gapX === '7', 'gap-x-8': props.gapX === '8', 'gap-x-9': props.gapX === '9', 'gap-x-10': props.gapX === '10', 'gap-x-11': props.gapX === '11', 'gap-x-12': props.gapX === '12', 'gap-y-0': props.gapY === '0', 'gap-y-px': props.gapY === 'px', 'gap-y-0.5': props.gapY === '0.5', 'gap-y-1': props.gapY === '1', 'gap-y-1.5': props.gapY === '1.5', 'gap-y-2': props.gapY === '2', 'gap-y-2.5': props.gapY === '2.5', 'gap-y-3': props.gapY === '3', 'gap-y-3.5': props.gapY === '3.5', 'gap-y-4': props.gapY === '4', 'gap-y-5': props.gapY === '5', 'gap-y-6': props.gapY === '6', 'gap-y-7': props.gapY === '7', 'gap-y-8': props.gapY === '8', 'gap-y-9': props.gapY === '9', 'gap-y-10': props.gapY === '10', 'gap-y-11': props.gapY === '11', 'gap-y-12': props.gapY === '12',}">
        <slot/>
    </Component>
</template>
