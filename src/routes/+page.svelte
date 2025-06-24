<script lang="ts">
    import { ContactIcons } from "$lib";
    import { fade, slide } from "svelte/transition";
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
        class="flex mt-10 flex-1 flex-col"
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

        <div class="flex justify-center">
            <a
            href="/resume.pdf"
            class="max-w-[220px] mt-8 py-3 bg-black text-white rounded-full text-lg font-medium shadow mb-8 hover:bg-gray-900 transition flex-1 text-center"
            in:fade={{ delay: 400, duration: 1000 }}
            >
            My Resume
            </a>
        </div>
    </div>
</main>
