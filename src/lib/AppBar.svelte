<script lang="ts">
    import { page } from "$app/stores";
</script>

<nav
    class="w-full bg-white shadow-none border-b border-gray-200 fixed top-0 left-0 z-30"
>
    <div class="max-w-2xl mx-auto flex items-center justify-center h-16">
        <a
            href="/"
            class="px-6 py-2 text-lg font-semibold text-gray-900 hover:text-black transition-colors duration-200
                {$page.url.pathname === `/`
                ? 'border-b-2 border-black'
                : 'border-b-2 border-transparent'}"
        >
            Home
        </a>
        <a
            href="/projects"
            class="px-6 py-2 text-lg font-semibold text-gray-900 hover:text-black transition-colors duration-200
                {$page.url.pathname === `/projects`
                ? 'border-b-2 border-black'
                : 'border-b-2 border-transparent'}"
        >
            Projects
        </a>
    </div>
</nav>
