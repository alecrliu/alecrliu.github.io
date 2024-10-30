<script lang="ts">
    import {base, AppBar, Button} from '$lib';
</script>
<style>
    .app-bar {
        width: 100%;
        background-color: #333;
        color: white;
        padding: 1rem;
        display: flex;
        justify-content: space-between;
    }

    .app-bar a {
        color: white;
        text-decoration: none;
        margin: 0 1rem;
    }

    .app-bar a:hover {
        text-decoration: underline;
    }
</style>

<AppBar>
    <div class="app-bar">
    <a href="{base}/">Home</a>
    <a href="{base}/projects">Projects</a>
    </div>
</AppBar>
<h1>Hello, this website looks really bad right now... BUT i fix soon.</h1>