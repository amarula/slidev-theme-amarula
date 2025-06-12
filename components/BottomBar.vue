<script>
</script>

<template>
    <div class="bottom-bar flex-items-center">
        <dev class="w-1/3 flex justify-start">
            {{ $slidev.configs.author || '' }} <div class="divider"></div> Amarula Solutions
        </dev>
        <dev class="w-1/3 flex justify-center">
            {{ $slidev.configs.event || '' }}
        </dev>
        <dev class="w-1/3 flex justify-end">
            <div>
                <SlideCurrentNo /> /
                <SlidesTotal />
            </div>
        </dev>
    </div>
</template>

<style scoped>
.divider {
    width: 1px;
    height: 1em;
    background-color: black;
    margin: 3px 10px;
}
</style>