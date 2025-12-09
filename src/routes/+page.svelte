<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
	import { goto } from '$app/navigation';

	function learnmore() {
		goto('/features');
	}
</script>

<svelte:head>
	<title>Recon Ball</title>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<!-- Decorative Background Elements -->
<div class="bg-decoration">
	<div class="circle circle-1"></div>
	<div class="circle circle-2"></div>
	<div class="circle circle-3"></div>
</div>

<main>
	<!-- First Card -->
	<div class="card card-small">
		<div class="badge">
			<svg
				width="48"
				height="48"
				viewBox="0 0 24 24"
				fill="none"
				stroke="currentColor"
				stroke-width="2"
			>
				<ellipse cx="12" cy="14" rx="5" ry="6" />
				<circle cx="12" cy="6" r="1.5" />
				<path d="M12 4.5V7.5" />
				<path d="M14 7C15 6.5 16 6 16 4.5" />
				<line x1="9" y1="20" x2="9" y2="20.5" />
				<line x1="12" y1="20.5" x2="12" y2="21" />
				<line x1="15" y1="20" x2="15" y2="20.5" />
			</svg>
		</div>

		<h1 class="header">Recon Ball</h1>
		<div class="divider"></div>
		<p class="header-text">
			A decoy-grenade made to confuse enemies and also count the no. of enemy soldiers
		</p>

		<div class="tags">
			<span class="tag">Tactical</span>
			<span class="tag">Intelligence</span>
			<span class="tag">Stealth</span>
		</div>
	</div>

	<!-- Second Card -->
	<div class="card card-large">
		<h1 class="header">How It Works</h1>
		<div class="divider"></div>

		<div class="columns">
			<div class="column">
				<h3>Detection</h3>
				<p>
					Utilizes many cameras to get a 360 degree view of the surroundings, without leaving any blinz spots
				</p>
			</div>
			<div class="column">
				<h3>Trained AI</h3>
				<p>
					Employs advanced machine learning algorithms to accurately identify and classify enemy soldiers in various environments.
				</p>
			</div>
			<div class="column">
				<h3>Data Collection</h3>
				<p>
					Counts and analyzes enemy soldier positions, transmitting critical reconnaissance data
					back to command center.
				</p>
			</div>
		</div>
	</div>

	<div>
		<div>
			<h1 class="header">Want to know more?</h1>
		</div>
		<div class="buttons">
			<button class="btn-primary" onclick={learnmore}>
				Learn more
				<svg
					width="20"
					height="20"
					viewBox="0 0 24 24"
					fill="none"
					stroke="currentColor"
					stroke-width="2"
				>
					<path d="M5 12H19M12 5l7 7-7 7" />
				</svg>
			</button>
		</div>
	</div>

	<Footer />
</main>

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Poppins', sans-serif;
		background: linear-gradient(135deg, #e8f5e9 0%, #f1f8f4 50%, #e0f2e8 100%);
		min-height: 100vh;
		overflow-x: hidden;
	}

	.buttons {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		justify-content: center;
		align-items: center;
		margin-bottom: 3rem;
	}

	@media (min-width: 640px) {
		.buttons {
			flex-direction: row;
		}
	}

	button {
		display: flex;
		align-items: center;
		gap: 0.5rem;
		padding: 0.75rem 1.5rem;
		border-radius: 0.5rem;
		font-weight: 500;
		transition: all 0.2s;
		cursor: pointer;
		border: none;
		font-size: 1rem;
	}

	.btn-primary {
		background-color: #00994d;
		color: white;
		box-shadow: 0 10px 15px -3px rgba(0, 148, 217, 0.3);
	}

	.btn-primary:hover {
		transform: scale(1.05);
		box-shadow: 0 20px 25px -5px rgba(0, 148, 217, 0.3);
	}

	.btn-primary:active {
		transform: scale(0.95);
	}

	.circle {
		position: absolute;
		border-radius: 50%;
		background: radial-gradient(circle, rgba(0, 153, 77, 0.08), transparent);
		animation: float 8s ease-in-out infinite;
	}

	.circle-1 {
		width: 500px;
		height: 500px;
		top: -150px;
		right: -100px;
		animation-delay: 0s;
	}

	.circle-2 {
		width: 350px;
		height: 350px;
		bottom: -100px;
		left: -80px;
		animation-delay: 2s;
	}

	.circle-3 {
		width: 250px;
		height: 250px;
		top: 40%;
		left: 20%;
		animation-delay: 4s;
	}

	@keyframes float {
		0%,
		100% {
			transform: translateY(0) scale(1);
		}
		50% {
			transform: translateY(-30px) scale(1.05);
		}
	}

	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 3rem;
		position: relative;
		z-index: 10;
		max-width: 1200px;
		margin: 0 auto;
		padding: 2rem;
		min-height: 100vh;
	}

	.card {
		background: white;
		padding: 3rem;
		border-radius: 20px;
		box-shadow: 0 10px 40px rgba(0, 153, 77, 0.1);
		text-align: center;
		transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
		border: 2px solid transparent;
		position: relative;
		overflow: hidden;
		margin-bottom: 3rem;
		width: 100%;
	}

	.card-small {
		max-width: 600px;
	}

	.card-large {
		max-width: 900px;
	}

	.card::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		height: 5px;
		background: linear-gradient(90deg, #00994d, #00cc66, #00994d);
		background-size: 200% 100%;
		animation: shimmer 3s linear infinite;
	}

	@keyframes shimmer {
		0% {
			background-position: -200% 0;
		}
		100% {
			background-position: 200% 0;
		}
	}

	.card:hover {
		transform: translateY(-10px);
		box-shadow: 0 20px 60px rgba(0, 153, 77, 0.2);
		border-color: #00994d;
	}

	.badge {
		width: 80px;
		height: 80px;
		margin: 0 auto 1.5rem;
		background: linear-gradient(135deg, #00994d, #00cc66);
		border-radius: 20%;
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		box-shadow: 0 8px 24px rgba(0, 153, 77, 0.3);
		transition: all 0.3s;
	}

	.card:hover .badge {
		box-shadow: 0 12px 32px rgba(0, 153, 77, 0.4);
	}

	.header {
		margin: 0.5rem 0;
		font-size: 2.5rem;
		font-weight: 700;
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		transition: all 0.3s;
		letter-spacing: -0.5px;
	}

	.card:hover .header {
		transform: scale(1.05);
	}

	.divider {
		width: 80px;
		height: 4px;
		background: linear-gradient(90deg, transparent, #00994d, transparent);
		margin: 1.5rem auto;
		border-radius: 2px;
		transition: all 0.3s;
	}

	.card:hover .divider {
		width: 120px;
	}

	.header-text {
		margin: 1.5rem 0;
		font-size: 1.1rem;
		color: #333;
		line-height: 1.7;
		transition: all 0.3s;
	}

	.card:hover .header-text {
		color: #00994d;
	}

	.tags {
		display: flex;
		gap: 0.8rem;
		justify-content: center;
		flex-wrap: wrap;
		margin: 2rem 0;
	}

	.tag {
		padding: 0.5rem 1.2rem;
		background: linear-gradient(135deg, rgba(0, 153, 77, 0.1), rgba(0, 204, 102, 0.1));
		color: #00994d;
		border-radius: 10px;
		font-size: 0.9rem;
		font-weight: 500;
		border: 1px solid rgba(0, 153, 77, 0.2);
		transition: all 0.3s;
	}

	.tag:hover {
		background: #00994d;
		color: white;
		transform: translateY(-2px);
		box-shadow: 0 4px 12px rgba(0, 153, 77, 0.3);
	}

	.columns {
		display: flex;
		gap: 2rem;
		justify-content: space-between;
		margin-top: 2rem;
	}

	.column {
		flex: 1;
		text-align: left;
		padding: 0 1.5rem;
		border-right: 2px solid rgba(0, 153, 77, 0.2);
	}

	.column:last-child {
		border-right: none;
	}

	.column h3 {
		font-size: 1.2rem;
		font-weight: 600;
		color: #00994d;
		margin-bottom: 0.8rem;
	}

	.column p {
		font-size: 0.95rem;
		color: #666;
		line-height: 1.6;
	}

	@media (max-width: 768px) {
		main {
			padding: 1rem;
		}

		.card {
			padding: 2rem 1.5rem;
		}

		.header {
			font-size: 2rem;
		}

		.header-text {
			font-size: 1rem;
		}

		.badge {
			width: 64px;
			height: 64px;
		}

		.badge svg {
			width: 32px;
			height: 32px;
		}

		.columns {
			flex-direction: column;
			gap: 1.5rem;
		}
	}
</style>
