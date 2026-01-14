<script lang="ts">
    import { fade, slide } from "svelte/transition";
    import { ProjectTiles } from "$lib";

    const projects = [
        {
            title: "YTubeDB",
            description: "A simplified YouTube clone.",
            image: "/example.png",
            site: "https://example.com",
            source: "https://gitlab.com/cs331e1/ytubedb",
        },
        {
            title: "Apples",
            description: "Another project that I made.",
            image: "/example.png",
            site: "https://example.com",

            source: "https://github.com/yourusername/project-repo",
        },
        {
            title: "Oranges",
            description: "Another one of my projects.",
            image: "/example.png",
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
            class="text-blue-500 dark:text-blue-400"
        >
            <path d="M12 2L2 7v10l10 5 10-5V7z" />
            <path d="M12 22V12" />
        </svg>
    </div>
    <p
        class="text-center text-xl text-gray-500 dark:text-gray-400 mb-8 font-light"
        in:fade={{ delay: 100, duration: 600 }}
    >
        A selection of things I've built or contributed to.
    </p>
    <div class="mb-8" in:slide={{ delay: 200, duration: 700 }}>
        <ProjectTiles {projects} />
    </div>
</main>
