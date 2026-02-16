<script>
	let waterCount = 0;
	let pressTimer = null;
	const LONG_PRESS_DURATION = 500; // milliseconds

	function handleTapStart() {
		// Start timer for long press detection
		pressTimer = setTimeout(() => {
			resetWater();
		}, LONG_PRESS_DURATION);
	}

	function handleTapEnd() {
		// If timer is still running, it was a short tap
		if (pressTimer !== null) {
			clearTimeout(pressTimer);
			incrementWater();
		}
	}

	function handleTapCancel() {
		// Clear timer if touch is cancelled
		if (pressTimer !== null) {
			clearTimeout(pressTimer);
		}
	}

	function incrementWater() {
		if (waterCount < 8) {
			waterCount++;
			playSound('tap');
		}
	}

	function resetWater() {
		waterCount = 0;
		playSound('reset');
		pressTimer = null;
	}

	/**
	 * @param {'tap' | 'reset'} soundType
	 */
	function playSound(soundType) {
		// Create audio context for sound
		const AudioContextClass = window.AudioContext || window.webkitAudioContext;
		const audioContext = new AudioContextClass();
		const oscillator = audioContext.createOscillator();
		const gainNode = audioContext.createGain();

		oscillator.connect(gainNode);
		gainNode.connect(audioContext.destination);

		if (soundType === 'tap') {
			// Higher pitch for tap
			oscillator.frequency.value = 800;
			gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
			gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.1);
		} else {
			// Lower pitch for reset
			oscillator.frequency.value = 400;
			gainNode.gain.setValueAtTime(0.3, audioContext.currentTime);
			gainNode.gain.exponentialRampToValueAtTime(0.01, audioContext.currentTime + 0.3);
		}

		oscillator.start(audioContext.currentTime);
		oscillator.stop(audioContext.currentTime + (soundType === 'tap' ? 0.1 : 0.3));
	}
</script>

<section>
	<div 
		class="water-tracker"
		on:mousedown={handleTapStart}
		on:mouseup={handleTapEnd}
		on:mouseleave={handleTapCancel}
		on:touchstart={handleTapStart}
		on:touchend={handleTapEnd}
		on:touchcancel={handleTapCancel}
		role="button"
		tabindex="0"
	>
		<h3 class="card-title">Water Tracker</h3>
		{#each Array(8) as _, i}
			<img 
				src="src/lib/assets/ui/droplet.png" 
				alt="water droplet icon" 
				class="droplet-icon"
				class:filled={i < waterCount}
			>
		{/each}
	</div>
</section>

<style>
	.water-tracker {
		background-color: #E43393;
		border-radius: 20px;
		border: 1px solid #191435;
		padding: 5px;
		text-align: center;
		box-shadow: 5px 5px #6dd5fa;
		width: 175px;
		height: 175px;
		cursor: pointer;
		user-select: none;
	}

	.card-title {
		font-size: 30px;
		margin-top: 3px;
		color: #6b1f8c;
		text-shadow: 2px 2px 15px #ffffff;
		font-family: 'Handjet';
		font-weight: 800;
		letter-spacing: 0.05em;
	}

	.droplet-icon {
		width: 40px;
		height: 40px;
		transition: opacity 0.2s ease;
		opacity: 0.3;
	}

	.droplet-icon.filled {
		opacity: 1;
	}
</style>