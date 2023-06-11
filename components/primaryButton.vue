<template>
    <nuxt-link :to="page" class="primary-button flex">
        {{text}}
        <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg">
            <path d="M3.75 12H20.25" stroke="#E3FF34" stroke-linecap="round" stroke-linejoin="round"/>
            <path d="M13.5 5.25L20.25 12L13.5 18.75" stroke="#E3FF34" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
    </nuxt-link>
</template>
<script>
    export default {
        name: 'external-button',
        props: ['page', 'text']
    }
</script>

<style lang="scss" scoped>

a {
    font-size: 24px;
    text-decoration: none;
    color: $accent-yellow;
    transition: .3s ease-in-out;
    align-items: flex-start;
    svg {
        margin-left: 8px;
        transition: .3s ease-in-out;
    }
    &:hover {
        color: darken($color: $accent-yellow, $amount: 30%);
        svg {
            margin-left: 12px;
            path {
                stroke: darken($color: $accent-yellow, $amount: 30%);;
            }
        }
    }
}

</style>