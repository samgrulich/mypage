<script lang="ts">
    export let href: string|undefined = undefined;
</script>

<style>
    div {
        padding: 0;
        height: 90px;
        width: fit-content;
        border-radius: 2rem;
        background-color: #f0f0f0;
    }
    a {
        width: inherit;
        height: inherit;
        margin: 0;
        padding: 0;
    }
</style>

<div>
<a {href}>
    <slot/>
</a>
</div>
