<script>
    import "../app.css";
    import { AppBar } from "$lib";
</script>

<AppBar />
<slot></slot>

<style>
    :global(body) {
        background: linear-gradient(135deg, #f8fafc 0%, #e0e7ef 100%);
    }
</style>
