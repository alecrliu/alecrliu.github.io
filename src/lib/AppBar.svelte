<script lang="ts">
    import { page } from "$app/stores";
    import ThemeToggle from "./ThemeToggle.svelte";
</script>

<nav
    class="w-full bg-white dark:bg-gray-900 shadow-none border-b border-gray-200 dark:border-gray-700 fixed top-0 left-0 z-30 transition-colors duration-200 h-16"
>
    <div class="relative w-full flex items-center h-16 px-4">
        <div class="flex items-center z-10">
            <ThemeToggle />
        </div>
        <div
            class="absolute left-1/2 top-1/2 -translate-x-1/2 -translate-y-1/2 flex items-center"
        >
            <a
                href="/"
                class="px-6 py-2 text-lg font-semibold text-gray-900 dark:text-white hover:text-black dark:hover:text-gray-300 transition-colors duration-200
                    {$page.url.pathname === `/`
                    ? 'border-b-2 border-black dark:border-white'
                    : 'border-b-2 border-transparent'}"
            >
                Home
            </a>
            <a
                href="/projects"
                class="px-6 py-2 text-lg font-semibold text-gray-900 dark:text-white hover:text-black dark:hover:text-gray-300 transition-colors duration-200
                    {$page.url.pathname === `/projects`
                    ? 'border-b-2 border-black dark:border-white'
                    : 'border-b-2 border-transparent'}"
            >
                Projects
            </a>
        </div>
        <div class="flex-1"></div>
    </div>
</nav>
