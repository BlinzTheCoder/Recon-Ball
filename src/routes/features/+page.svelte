 <script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
	<title>Features - Recon Ball</title>
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
	<div class="section-header">
		<h1 class="title">Key Features</h1>
		<div class="divider"></div>
		<p class="subtitle">Cutting-edge technology for tactical superiority</p>
	</div>

	<!-- Main Feature Grid -->
	<div class="features-grid">
		<div class="feature-card large">
			<div class="icon-badge">
				<svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<circle cx="12" cy="12" r="10"/>
					<circle cx="12" cy="12" r="3"/>
					<line x1="12" y1="1" x2="12" y2="3"/>
					<line x1="12" y1="21" x2="12" y2="23"/>
					<line x1="4.22" y1="4.22" x2="5.64" y2="5.64"/>
					<line x1="18.36" y1="18.36" x2="19.78" y2="19.78"/>
					<line x1="1" y1="12" x2="3" y2="12"/>
					<line x1="21" y1="12" x2="23" y2="12"/>
					<line x1="4.22" y1="19.78" x2="5.64" y2="18.36"/>
					<line x1="18.36" y1="5.64" x2="19.78" y2="4.22"/>
				</svg>
			</div>
			<h2>360° Vision System</h2>
			<p>Multiple cameras provide complete spherical coverage, eliminating blind spots and ensuring comprehensive battlefield awareness.</p>
		</div>

		<div class="feature-card">
			<div class="icon-badge">
				<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<rect x="3" y="3" width="18" height="18" rx="2"/>
					<path d="M9 3v18"/>
					<path d="m16 15-3-3 3-3"/>
				</svg>
			</div>
			<h3>AI-Powered Recognition</h3>
			<p>Advanced machine learning algorithms accurately identify and count enemy personnel with near-perfect precision.</p>
		</div>

		<div class="feature-card">
			<div class="icon-badge">
				<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<path d="M12 2a10 10 0 1 0 10 10H12V2z"/>
					<path d="M2 12h10v10"/>
				</svg>
			</div>
			<h3>Tactical Deception</h3>
			<p>Realistic grenade mimicry confuses adversaries, creating strategic diversions and protecting your team.</p>
		</div>

		<div class="feature-card">
			<div class="icon-badge">
				<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<path d="M12 2v20M2 12h20"/>
					<circle cx="12" cy="12" r="10"/>
				</svg>
			</div>
			<h3>Transmitter</h3>
			<p>Nrf24L01 is the transmitter used by Recon Ball with 1km range and 32 bits of storage which is more than sufficient</p>
		</div>

		<div class="feature-card">
			<div class="icon-badge">
				<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
					<path d="M13 2L3 14h9l-1 8 10-12h-9l1-8z"/>
				</svg>
			</div>
			<h3>Good Battery Life</h3>
			<p>Recon Ball is powered by a 6040mah battery ensuring the ball can work for atleast 6 hours</p>
		</div>
	</div>

	<!-- Technical Specifications -->
	<div class="specs-section">
		<h2 class="specs-title">Technical Specifications</h2>
		<div class="specs-grid">
			<div class="spec-item">
				<span class="spec-label">Weight</span>
				<span class="spec-value">450g</span>
			</div>
			<div class="spec-item">
				<span class="spec-label">Diameter</span>
				<span class="spec-value">5 cm</span>
			</div>
			<div class="spec-item">
				<span class="spec-label">Battery Life</span>
				<span class="spec-value">6 hours</span>
			</div>
			<div class="spec-item">
				<span class="spec-label">Range</span>
				<span class="spec-value">1km</span>
			</div>
			<div class="spec-item">
				<span class="spec-label">Cameras</span>
				<span class="spec-value">4 x 2MP</span>
			</div>
		</div>
	</div>
</main>
<Footer />

<style>
	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Poppins', sans-serif;
		background: linear-gradient(135deg, #e8f5e9 0%, #f1f8f4 50%, #e0f2e8 100%);
		min-height: 100vh;
		overflow-x: hidden;
	}

	.bg-decoration {
		position: fixed;
		inset: 0;
		pointer-events: none;
		z-index: 1;
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
		0%, 100% {
			transform: translateY(0) scale(1);
		}
		50% {
			transform: translateY(-30px) scale(1.05);
		}
	}

	main {
		max-width: 1200px;
		margin: 0 auto;
		padding: 4rem 2rem;
		position: relative;
		z-index: 10;
	}

	.section-header {
		text-align: center;
		margin-bottom: 4rem;
	}

	.title {
		font-size: 3rem;
		font-weight: 700;
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		margin-bottom: 1rem;
		letter-spacing: -0.5px;
	}

	.divider {
		width: 80px;
		height: 4px;
		background: linear-gradient(90deg, transparent, #00994d, transparent);
		margin: 1.5rem auto;
		border-radius: 2px;
	}

	.subtitle {
		font-size: 1.2rem;
		color: #666;
		margin: 0;
	}

	.features-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
		gap: 2rem;
		margin-bottom: 4rem;
	}

	.feature-card {
		background: white;
		padding: 2.5rem;
		border-radius: 20px;
		box-shadow: 0 10px 40px rgba(0, 153, 77, 0.1);
		border: 2px solid transparent;
		position: relative;
		overflow: hidden;
		transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
	}

	.feature-card.large {
		grid-column: span 2;
	}

	.feature-card::before {
		content: '';
		position: absolute;
		top: 0;
		left: 0;
		right: 0;
		height: 4px;
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

	.feature-card:hover {
		transform: translateY(-10px);
		box-shadow: 0 20px 60px rgba(0, 153, 77, 0.2);
		border-color: #00994d;
	}

	.icon-badge {
		width: 70px;
		height: 70px;
		background: linear-gradient(135deg, rgba(0, 153, 77, 0.1), rgba(0, 204, 102, 0.1));
		border-radius: 15px;
		display: flex;
		align-items: center;
		justify-content: center;
		color: #00994d;
		margin-bottom: 1.5rem;
		transition: all 0.3s;
	}

	.feature-card:hover .icon-badge {
		background: linear-gradient(135deg, #00994d, #00cc66);
		color: white;
		transform: scale(1.1);
	}

	.feature-card h2 {
		font-size: 1.8rem;
		font-weight: 600;
		color: #333;
		margin-bottom: 1rem;
		transition: all 0.3s;
	}

	.feature-card h3 {
		font-size: 1.4rem;
		font-weight: 600;
		color: #333;
		margin-bottom: 1rem;
		transition: all 0.3s;
	}

	.feature-card:hover h2,
	.feature-card:hover h3 {
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
	}

	.feature-card p {
		color: #666;
		line-height: 1.7;
		font-size: 0.95rem;
		margin-bottom: 1.5rem;
	}

	.feature-card ul {
		list-style: none;
		padding: 0;
		margin: 0;
	}

	.feature-card ul li {
		color: #666;
		padding: 0.6rem 0;
		padding-left: 1.8rem;
		position: relative;
		font-size: 0.95rem;
	}

	.feature-card ul li::before {
		content: '✓';
		position: absolute;
		left: 0;
		color: #00994d;
		font-weight: 700;
		font-size: 1.1rem;
	}

	.specs-section {
		background: white;
		padding: 3rem;
		border-radius: 20px;
		box-shadow: 0 10px 40px rgba(0, 153, 77, 0.1);
		border: 2px solid transparent;
		position: relative;
		overflow: hidden;
		transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
	}

	.specs-section::before {
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

	.specs-title {
		font-size: 2rem;
		font-weight: 600;
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		text-align: center;
		margin-bottom: 2.5rem;
	}

	.specs-grid {
		display: grid;
		grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
		gap: 2rem;
	}

	.spec-item {
		display: flex;
		flex-direction: column;
		align-items: center;
		text-align: center;
		padding: 1.5rem;
		background: linear-gradient(135deg, rgba(0, 153, 77, 0.05), rgba(0, 204, 102, 0.05));
		border-radius: 15px;
		transition: all 0.3s;
	}

	.spec-item:hover {
		background: linear-gradient(135deg, rgba(0, 153, 77, 0.1), rgba(0, 204, 102, 0.1));
		transform: translateY(-5px);
	}

	.spec-label {
		font-size: 0.9rem;
		color: #666;
		text-transform: uppercase;
		letter-spacing: 1px;
		margin-bottom: 0.5rem;
	}

	.spec-value {
		font-size: 1.8rem;
		font-weight: 700;
		color: #00994d;
	}

	@media (max-width: 968px) {
		.feature-card.large {
			grid-column: span 1;
		}

		.title {
			font-size: 2.5rem;
		}
	}

	@media (max-width: 640px) {
		main {
			padding: 2rem 1rem;
		}

		.section-header {
			margin-bottom: 3rem;
		}

		.title {
			font-size: 2rem;
		}

		.subtitle {
			font-size: 1rem;
		}

		.features-grid {
			grid-template-columns: 1fr;
			gap: 1.5rem;
		}

		.feature-card {
			padding: 2rem 1.5rem;
		}

		.specs-section {
			padding: 2rem 1.5rem;
		}

		.specs-grid {
			grid-template-columns: repeat(2, 1fr);
			gap: 1rem;
		}

		.spec-item {
			padding: 1rem;
		}

		.spec-value {
			font-size: 1.5rem;
		}
	}
</style>