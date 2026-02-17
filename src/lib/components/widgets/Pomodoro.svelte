<script>


</script>

<section>
<div class="timer">
    <h3 class="card-title"> Work Timer</h3>
<div class="container">      
    <div class="function-buttons">
        <button id="start">Start</button>
        <button id="pause">Pause</button>
      </div>
      <div class="progress">
          <h2 class="progress-number">25:00</h2>
      </div>
      <div class="bottom-buttons">
        <button id="shortbrk">Short</button>
        <button id="longbrk">Long</button>
        <button id="reset">Reset</button>
      </div>
    </div>
    </div>
</section>

<style>
    .timer {
        background-color: #E43393;
        border-radius: 20px;
        border: 1px solid #191435;
        padding: 5px;
        text-align: center;
        box-shadow: 5px 5px #6dd5fa;
        width: 175px;
        height: 175px;
        
    }

    .card-title {
        font-size: 30px;
        margin-top: 3px;
        margin-bottom: 10px;
        color: #6b1f8c;
        text-shadow: 2px 2px 15px #ffffff;
        font-family: 'Handjet';
        font-weight: 800;
        letter-spacing: 0.05em;
    }

    .function-buttons {
        display: flex;
        justify-content: center;
        gap: 10px;
        margin-top: 0px;
        border-radius: 20px;
    }

    .progress-number {
        font-size: 55px;
        font-family: 'Orbitron', sans-serif !important;
        color: #0F2164;
        margin-top: 5px;
        margin-bottom: 5px;
    }

    .bottom-buttons {
      margin-top: 0px;
    }

    button {
        border-radius: 5px;
    }

</style>