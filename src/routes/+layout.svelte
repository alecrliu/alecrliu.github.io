<script>
    import "../app.css";
    import { AppBar } from "$lib";
</script>

<AppBar />
<slot></slot>

<style>
    :global(body) {
        background-color: #f0f4f8;
        color: #333;
        transition:
            background-color 0.2s ease,
            color 0.2s ease;
    }

    :global(body.dark) {
        background-color: #1a1a1a;
        color: #e5e5e5;
    }
</style>
