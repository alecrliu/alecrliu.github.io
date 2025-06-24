<script lang="ts">
    import { fade } from "svelte/transition";
    import { base } from "$app/paths";
    import { ProjectTiles } from "$lib";

    const projects = [
        {
            title: "YTubeDB",
            description: ".",
            link: "https://github.com/yourusername/project-repo",
        },
        {
            title: "Title",
            description: ".",
            link: "https://github.com/yourusername/project-repo",
        },
    ];
</script>

<main class="flex flex-col min-h-screen max-w-2xl mx-auto mt-32 px-4">
    <h1
        class="text-5xl font-medium text-center mb-4 tracking-tight text-gray-900"
        in:fade={{ duration: 500 }}
    >
        Projects
    </h1>
    <p
        class="text-center text-xl text-gray-500 mb-8 font-light"
        in:fade={{ delay: 100, duration: 600 }}
    >
        A selection of things I've built or contributed to.
    </p>
    <ProjectTiles {projects} />
</main>
