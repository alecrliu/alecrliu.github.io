<script>
    import "../app.css";
    import { AppBar } from "$lib";
</script>
<style>
    :global(body) {
        background-color: #f0f4f8;
        color: #333;
    }
</style>
<AppBar />
<slot></slot>
