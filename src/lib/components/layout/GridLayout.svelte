<script>
import MoodPixel from '$lib/components/widgets/MoodPixel.svelte';
import PhotoRotate from '$lib/components/widgets/PhotoRotate.svelte';
import WaterCounter from '$lib/components/widgets/WaterCounter.svelte';

</script>

<style>
    .module{
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
        gap: 20px;
        justify-items: center;
        align-items: center;
    }
</style>

<div class="module">
    <MoodPixel />
    <PhotoRotate />
    <WaterCounter />
</div>