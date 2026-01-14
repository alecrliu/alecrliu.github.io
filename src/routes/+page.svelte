<script lang="ts">
    import { ContactIcons } from "$lib";
    import { fade } from "svelte/transition";
</script>

<svelte:head>
    <title>Alec's Portfolio</title>
</svelte:head>

<main class="flex-col min-h-screen min-w-screen mx-auto mt-32">
    <img
        src="/pixelduck.gif.webp"
        alt="Profile Icon"
        class="w-60 h-60 rounded-full mb-20 mx-auto shadow-lg"
        in:fade={{ duration: 500 }}
    />
    <h1
        class="text-5xl font-medium text-center mb-4 tracking-tight text-gray-900 dark:text-white"
        in:fade={{ delay: 100, duration: 600 }}
    >
        Hi, I'm Alec
    </h1>
    <div
        class="flex justify-center mb-16"
        in:fade={{ delay: 200, duration: 700 }}
    >
        <ContactIcons
            email="alec.liu.arl@gmail.com"
            github="https://github.com/alecrliu"
            linkedin="https://linkedin.com/in/alecrliu"
        />
    </div>
    <div
        class="flex mt-10 flex-1 flex-col"
        in:fade={{ delay: 600, duration: 800 }}
    >
        <p
            class="text-center text-xl text-gray-500 dark:text-gray-400 mb-2 font-light"
        >
            Mechanical engineering graduate. <br />
            Current computer science student. <br />
            Data-driven engineer. <br />
        </p>

        <div class="flex justify-center">
            <a
                href="/resume.pdf"
                class="max-w-[220px] mt-8 py-3 bg-black dark:bg-white text-white dark:text-black rounded-full text-lg font-medium shadow mb-8 hover:bg-gray-900 dark:hover:bg-gray-200 transition flex-1 text-center"
            >
                My Resume
            </a>
        </div>
    </div>
</main>
