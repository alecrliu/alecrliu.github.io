<script lang="ts">
    import { fade, slide } from "svelte/transition";
    import { ProjectTiles } from "$lib";

    const projects = [
        {
            title: "YTubeDB",
            description: "A simplified YouTube clone.",
            image: "/pixelduck.gif.webp",
            source: "https://github.com/yourusername/project-repo",
        },
        {
            title: "Apples",
            description: ".",
            image: "https://via.placeholder.com/150",
            source: "https://github.com/yourusername/project-repo",
        },
        {
            title: "Oranges",
            description: ".",
            image: "https://via.placeholder.com/150",
            site: "https://example.com",
            source: "https://github.com/alecrliu/project-repo",
        },
    ];
</script>

<svelte:head>
    <title>Alec's Projects</title>
</svelte:head>

<main class="flex-col min-h-screen mx-auto mt-40 px-8">
    <div class="justify-center flex mb-8" in:fade={{ duration: 500 }}>
        <svg
            width="64"
            height="64"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-blue-500"
        >
            <path d="M12 2L2 7v10l10 5 10-5V7z" />
            <path d="M12 22V12" />
        </svg>
        <svg
            width="64"
            height="64"
            viewBox="0 0 24 24"
            fill="none"
            stroke="currentColor"
            stroke-width="2"
            stroke-linecap="round"
            stroke-linejoin="round"
            class="text-blue-500"
        >
            <rect x="3" y="3" width="7" height="7" />
            <rect x="14" y="3" width="7" height="7" />
            <rect x="14" y="14" width="7" height="7" />
            <rect x="3" y="14" width="7" height="7" />
        </svg>
    </div>
    <p
        class="text-center text-xl text-gray-500 mb-8 font-light"
        in:fade={{ delay: 100, duration: 600 }}
    >
        A selection of things I've built or contributed to.
    </p>
    <div class="" in:slide={{ delay: 200, duration: 700 }}>
        <ProjectTiles {projects} />
    </div>
</main>
