<script lang="ts">
    import { slide } from "svelte/transition";
    export let projects: Array<{
        title: string;
        description: string;
        link: string;
    }> = [];
</script>

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
