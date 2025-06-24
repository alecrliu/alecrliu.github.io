<script lang="ts">
    import { fade, slide } from "svelte/transition";

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
    <div class="grid gap-6">
        {#each projects as project, i}
            <div
                class="p-6 bg-white/80 rounded-lg shadow hover:shadow-lg transition"
                in:slide={{ delay: 200 + i * 100, duration: 700 }}
            >
                <h2 class="text-2xl font-semibold mb-2 text-gray-900">
                    {project.title}
                </h2>
                <p class="text-gray-600 mb-4">{project.description}</p>
                <a
                    href={project.link}
                    target="_blank"
                    class="text-blue-600 hover:underline font-medium"
                >
                    View on GitHub
                </a>
            </div>
        {/each}
    </div>
</main>
