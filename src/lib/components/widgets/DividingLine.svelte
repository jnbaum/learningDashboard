<script>
    // optional prop to enable animated variant
   // export let anim = false;
</script>

<hr class = hr >
<!--<div class="hr" class:anim={anim} aria-hidden="true"></div>-->

<style>

.hr {
    border-bottom: 6px dotted #F2A950;
}



   /* I might fiddle with this later, but for now, I'm removing the dividing line animation
   
   :root {
        --bg: #191435;
        --barsize: 575px;
    }

    .hr {
        width: 100%;
        height: 5dvh;
        display: block;
        position: relative;
        margin-bottom: 0;
        padding: 2em 0;
    }

    .hr::before,
    .hr::after {
        content: "";
        position: absolute;
        width: 100%;
        height: 5px;
        bottom: 50%;
        left: 0;
    }

    .hr::before {
        background: linear-gradient(90deg, var(--bg) 0%, var(--bg) 50%, transparent 50%, transparent 100%);
        background-size: var(--barsize);
        background-position: center;
        z-index: 1;
    }

    .hr::after {
        transition: opacity 0.3s ease, animation 0.3s ease;
        background: linear-gradient(
            to right,
            #E43393 10%,
            #6B1F8C 25%,
            #A6296E 35%,
            #4B1659 45%,
            #F2A950 60%,
            #0F2164 80%,
            #FF8A4A 95%
        );

        background-color: #E43393;
        background-size: 200%;
        background-position: 0%;
        animation: bar 15s linear infinite;
    }

    @keyframes bar {
        0% { background-position: 0%; }
        100% { background-position: 200%; }
    }

    .hr.anim::before {
        background: linear-gradient(
            90deg,
            var(--bg) 0%, var(--bg) 5%,
            transparent 5%, transparent 10%,
            var(--bg) 10%, var(--bg) 15%,
            transparent 15%, transparent 20%,
            var(--bg) 20%, var(--bg) 25%,
            transparent 25%, transparent 30%,
            var(--bg) 30%, var(--bg) 35%,
            transparent 35%, transparent 40%,
            var(--bg) 40%, var(--bg) 45%,
            transparent 45%, transparent 50%,
            var(--bg) 50%, var(--bg) 55%,
            transparent 55%, transparent 60%,
            var(--bg) 60%, var(--bg) 65%,
            transparent 65%, transparent 70%,
            var(--bg) 70%, var(--bg) 75%,
            transparent 75%, transparent 80%,
            var(--bg) 80%, var(--bg) 85%,
            transparent 85%, transparent 90%,
            var(--bg) 90%, var(--bg) 95%,
            transparent 95%, transparent 100%
        );
        background-size: calc(var(--barsize) * 10);
        background-position: center;
        z-index: 1;
        animation: bar 120s linear infinite;
    }
*/
</style>


