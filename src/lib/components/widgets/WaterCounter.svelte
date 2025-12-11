<script>
    let water = 0;


    //one tap-increment water count and make a sound
    //long tap-reset water count and make a different sound
</script>

<section id = module>
<div class = waterTracker>
    <h3 class = cardTitle>Water Tracker</h3>
    <img src = "src/lib/assets/ui/droplet.png" alt = "water droplet icon" class = dropletIcon >
</div>
</section>

<style>
    .waterTracker {
        background-color: #E43393;
        border-radius: 20px;
        border: 1px solid #191435;
        padding: 5px;
        text-align: center;
        box-shadow: 5px 5px #6dd5fa;
        width: 180px;
        height: 180px;
        
    }

    .cardTitle {
        font-size: 24px;
        margin-top: 10px;
        color: #6b1f8c;
        text-shadow: 2px 2px 15px #ffffff;
    
    }

    .dropletIcon {
        width: 40px;
        height: 40px;
    }

</style>