<script lang="ts">
    import { base } from "$app/paths";
    import { page } from "$app/stores";
    import { TabGroup, Tab, TabAnchor } from "@skeletonlabs/skeleton";
</script>

<TabGroup
    justify="justify-center"
    active="variant-filled-primary"
    hover="hover:variant-soft-primary"
    flex="flex-1 lg:flex-none"
    rounded=""
    border=""
    class="bg-surface-100-800-token w-full"
>
    <TabAnchor href="{base}/" selected={$page.url.pathname === `${base}/`}>
        <svelte:fragment slot="lead"></svelte:fragment>
        <span>Home</span>
    </TabAnchor>
    <TabAnchor
        href="{base}/projects"
        selected={$page.url.pathname === `${base}/projects`}
    >
        <svelte:fragment slot="lead"></svelte:fragment>
        <span>Projects</span>
    </TabAnchor>
</TabGroup>
