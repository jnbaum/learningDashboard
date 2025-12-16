<script>
import Todo from '$lib/components/widgets/Todo.svelte';
import MoodPixel from '$lib/components/widgets/MoodPixel.svelte';
import PhotoRotate from '$lib/components/widgets/PhotoRotate.svelte';
import WaterCounter from '$lib/components/widgets/WaterCounter.svelte';
import DNDLight from '$lib/components/widgets/DNDLight.svelte';
import StretchReminder from '$lib/components/widgets/StretchReminder.svelte';
import StarAnimation from '$lib/components/visuals/StarAnimation.svelte';
import Pomodoro from '$lib/components/widgets/Pomodoro.svelte';
import HabitTracker from '$lib/components/widgets/HabitTracker.svelte';
import DividingLine from '$lib/components/widgets/DividingLine.svelte';

</script>

<style>

    .module{
        display: grid;
        position: fixed;
        left: 50%;
        transform: translateX(-50%);
        bottom: 50px;
        z-index: 50;
        width: 580px;
        max-width: 100%;
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
        gap: 12px;
        justify-items: center;
        align-items: center;
    }
</style>


<DividingLine />
<DividingLine />

<DividingLine />
<DividingLine />

<div class="module">
    <Todo />
    <WaterCounter />
    <DNDLight />
    <StretchReminder />
    <StarAnimation />
    <PhotoRotate />
    <Pomodoro />
    <HabitTracker />
    <MoodPixel />
</div>
<DividingLine />
<DividingLine />