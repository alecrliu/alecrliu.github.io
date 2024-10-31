<script lang="ts">
    export let href: string;
    export let className: string;
</script>
    
<a href={href} class={className}>
    <slot></slot>
</a>
