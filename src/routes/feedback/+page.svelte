<script>
	function feedbackform()
	{
		window.location.href = "https://forms.gle/sNS8NkgFuNLP7iu67"
	}
</script>

<svelte:head>
	<title>Recon Ball</title>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
	<link
		href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;500;600;700&display=swap"
		rel="stylesheet"
	/>bn1
</svelte:head>

<main>
	<div>
		<div>
			<h1 class="header">We would love to get some feeback from you!</h1>
		</div>
		<div class="buttons">
			<button class="btn-primary" onclick={feedbackform}>
				Feedback Form
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
</main>

<style>
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
	.btn-primary {
		background-color: #00994d;
		color: white;
		box-shadow: 0 10px 15px -3px rgba(0, 148, 217, 0.3);
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
	.btn-primary:hover {
		transform: scale(1.05);
		box-shadow: 0 20px 25px -5px rgba(0, 148, 217, 0.3);
	}

	.btn-primary:active {
		transform: scale(0.95);
	}
</style>
