<template>
    <label :for="n">
        <input type="radio" :id="n" name="rating" :value="n" />
        <span class="dot">{{ n }}</span>
    </label>
</template>

<script setup>

const props = defineProps({
    n: Number
})

</script>

<style lang="scss" scoped>
input[type="radio"] {
    position: absolute;
    opacity: 0;

    &+.dot {
        transition: all 0.2s ease-in-out;
        cursor: pointer;
        font-weight: 700;
    }

    &:hover+.dot {
        background-color: $color-primary-Orange;
        color: $color-neutral-White;
    }

    &:focus+.dot {
        background-color: $color-primary-Orange;
        color: $color-neutral-White;
    }

    &:checked+.dot {
        background-color: $color-neutral-Light-Grey;
        color: $color-neutral-White;
    }
}
</style>