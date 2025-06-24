<script lang="ts">
    import { ContactIcons } from "$lib";
    import { fade, slide } from "svelte/transition";
</script>

<svelte:head>
    <title>Alec's Portfolio</title>
</svelte:head>

<main class="flex-col min-h-screen max-w-2xl mx-auto mt-32 px-28">
    <img
        src="/pixelduck.gif.webp"
        alt="Profile Icon"
        class="w-60 h-60 rounded-full mb-20 mx-auto shadow-lg"
        in:fade={{ duration: 500 }}
    />
    <h1
        class="text-5xl font-medium text-center mb-4 tracking-tight text-gray-900"
        in:fade={{ delay: 100, duration: 600 }}
    >
        Hi, I'm Alec
    </h1>
    <div
        class="flex justify-center mb-20"
        in:fade={{ delay: 200, duration: 700 }}
    >
        <ContactIcons
            email="alec.liu.arl@gmail.com"
            github="https://github.com/alecrliu"
            linkedin="https://linkedin.com/in/alecrliu"
        />
    </div>
    <div
        class="mt-10 flex-1 flex flex-col justify-between"
        in:slide={{ delay: 600, duration: 800 }}
    >
        <p
            class="text-center text-xl text-gray-500 mb-2 font-light"
            in:fade={{ delay: 300, duration: 900 }}
        >
            Current computer science student. <br />
            Previous mechanical engineering graduate. <br />
            A full stack, engineering, and data Psyduck. <br />
        </p>
        <a
            href="/resume.pdf"
            class="justify-center flex mt-8 py-3 bg-black text-white rounded-full text-lg font-medium shadow hover:bg-gray-900 transition"
            download
            in:fade={{ delay: 400, duration: 1000 }}
        >
            Download Resume
        </a>
    </div>
</main>
