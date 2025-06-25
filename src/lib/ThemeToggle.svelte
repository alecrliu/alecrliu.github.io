<script lang="ts">
    import { writable } from "svelte/store";
    import { browser } from "$app/environment";

    // Get initial theme from localStorage or default to 'light'
    const getInitialTheme = () => {
        if (browser) {
            const saved = localStorage.getItem("theme");
            if (saved) return saved;

            // Check system preference
            if (window.matchMedia("(prefers-color-scheme: dark)").matches) {
                return "dark";
            }
        }
        return "light";
    };

    // Create the store
    const theme = writable(getInitialTheme());

    // Subscribe to theme changes and update localStorage and document
    if (browser) {
        theme.subscribe((value) => {
            localStorage.setItem("theme", value);

            if (value === "dark") {
                document.documentElement.classList.add("dark");
                document.body.setAttribute("data-theme", "wintry");
            } else {
                document.documentElement.classList.remove("dark");
                document.body.setAttribute("data-theme", "wintry");
            }
        });
    }

    // Toggle function
    function toggleTheme() {
        theme.update((current) => (current === "light" ? "dark" : "light"));
    }
</script>

<button
    on:click={toggleTheme}
    class="p-2 rounded-lg bg-gray-100 dark:bg-gray-800 hover:bg-gray-200 dark:hover:bg-gray-700 transition-colors duration-200"
    aria-label="Toggle dark mode"
>
    {#if $theme === "dark"}
        <!-- Sun icon for dark mode -->
        <svg
            class="w-5 h-5 text-yellow-500"
            fill="currentColor"
            viewBox="0 0 20 20"
        >
            <path
                fill-rule="evenodd"
                d="M10 2a1 1 0 011 1v1a1 1 0 11-2 0V3a1 1 0 011-1zm4 8a4 4 0 11-8 0 4 4 0 018 0zm-.464 4.95l.707.707a1 1 0 001.414-1.414l-.707-.707a1 1 0 00-1.414 1.414zm2.12-10.607a1 1 0 010 1.414l-.706.707a1 1 0 11-1.414-1.414l.707-.707a1 1 0 011.414 0zM17 11a1 1 0 100-2h-1a1 1 0 100 2h1zm-7 4a1 1 0 011 1v1a1 1 0 11-2 0v-1a1 1 0 011-1zM5.05 6.464A1 1 0 106.465 5.05l-.708-.707a1 1 0 00-1.414 1.414l.707.707zm1.414 8.486l-.707.707a1 1 0 01-1.414-1.414l.707-.707a1 1 0 011.414 1.414zM4 11a1 1 0 100-2H3a1 1 0 000 2h1z"
                clip-rule="evenodd"
            ></path>
        </svg>
    {:else}
        <!-- Moon icon for light mode -->
        <svg
            class="w-5 h-5 text-gray-700"
            fill="currentColor"
            viewBox="0 0 20 20"
        >
            <path
                d="M17.293 13.293A8 8 0 016.707 2.707a8.001 8.001 0 1010.586 10.586z"
            ></path>
        </svg>
    {/if}
</button>
