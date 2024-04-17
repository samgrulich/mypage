<script lang="ts">
    export let href: string|undefined = undefined;
    export let size: number = 80;
</script>

<style>
    div {
        padding: 0;
        height: calc(var(--size) * 1px);
        width: fit-content;
        border-radius: 1rem;
        background-color: #f0f0f0;
    }
    a {
        width: inherit;
        height: inherit;
        margin: 0;
        padding: 0;
    }
</style>

<div style='--size:{size}'>
<a {href}>
    <slot/>
</a>
</div>
