<script lang="ts">
    export let projects: Array<{
        title: string;
        image?: string;
        description: string;
        source?: string;
        site?: string;
    }> = [];
</script>

<div class="grid grid-cols-1 md:grid-cols-2 gap-5">
    {#each projects as project}
        <div
            class="p-4 bg-white/80 dark:bg-gray-800/80 rounded-lg shadow hover:shadow-lg transition"
        >
            <div class="flex flex-col items-center">
                <h2
                    class="text-2xl font-semibold mb-4 text-gray-900 dark:text-white text-center"
                >
                    {project.title}
                </h2>
                {#if project.image}
                    <img
                        src={project.image}
                        alt={project.title}
                        class="object-cover rounded mb-6"
                    />
                {/if}

                <p class="text-gray-500 dark:text-gray-400 mb-4">
                    {project.description}
                </p>
            </div>
            <div class="flex justify-between">
                {#if project.source}
                    <a
                        href={project.source}
                        target="_blank"
                        class="text-blue-600 dark:text-blue-400 hover:underline font-medium"
                    >
                        Source
                    </a>
                {/if}
                <div class="flex-1"></div>
                {#if project.site}
                    <a
                        href={project.site}
                        target="_blank"
                        class="text-blue-600 dark:text-blue-400 hover:underline font-medium"
                    >
                        Site
                    </a>
                {/if}
            </div>
        </div>
    {/each}
</div>
