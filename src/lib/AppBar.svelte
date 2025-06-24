<script lang="ts">
    import { base } from "$app/paths";
    import { page } from "$app/stores";
</script>

<nav
    class="w-full bg-white/70 backdrop-blur-lg shadow-none border-b border-gray-200 fixed top-0 left-0 z-30"
>
    <div class="max-w-2xl mx-auto flex items-center justify-center h-16">
        <a
            href="{base}/"
            class="px-6 py-2 text-lg font-semibold text-gray-900 hover:text-black transition-colors duration-200
                {$page.url.pathname === `${base}/`
                ? 'border-b-2 border-black'
                : 'border-b-2 border-transparent'}"
        >
            Home
        </a>
        <a
            href="{base}/projects"
            class="px-6 py-2 text-lg font-semibold text-gray-900 hover:text-black transition-colors duration-200
                {$page.url.pathname === `${base}/projects`
                ? 'border-b-2 border-black'
                : 'border-b-2 border-transparent'}"
        >
            Projects
        </a>
    </div>
</nav>
