<script>
import Header from '$lib/header.svelte'
import '../tailwind.css';
</script>

<Header />

<main class="bg-blue-400">
    <slot />
</main >
<footer>Copywrite 2021</footer>

<!-- can do global like below but better to scope in each file, 
    we don't have to add a class to eveything if we add styles 
    to every file -->
<!-- <style>
    :global(header) {
        background: red;
    }
</style> -->