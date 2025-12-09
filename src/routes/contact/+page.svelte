<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
</script>

<svelte:head>
	<title>Contact Us - Recon Ball</title>
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
		<h1 class="title">Get In Touch</h1>
		<div class="divider"></div>
		<p class="subtitle">Have questions about Recon Ball? We'd love to hear from you.</p>
	</div>

	<div class="contact-container">
		<!-- Contact Info -->
		<div class="info-section-full">
			<div class="info-card">
				<div class="icon-wrapper">
					<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
						<path d="M21 10c0 7-9 13-9 13s-9-6-9-13a9 9 0 0 1 18 0z"/>
						<circle cx="12" cy="10" r="3"/>
					</svg>
				</div>
				<h3>Visit Us</h3>
				<p>Manav Rachan Internation School<br/>Sector-46 Gurgaon<br/>Haryana</p>
			</div>

			<div class="info-card">
				<div class="icon-wrapper">
					<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
						<path d="M22 16.92v3a2 2 0 0 1-2.18 2 19.79 19.79 0 0 1-8.63-3.07 19.5 19.5 0 0 1-6-6 19.79 19.79 0 0 1-3.07-8.67A2 2 0 0 1 4.11 2h3a2 2 0 0 1 2 1.72 12.84 12.84 0 0 0 .7 2.81 2 2 0 0 1-.45 2.11L8.09 9.91a16 16 0 0 0 6 6l1.27-1.27a2 2 0 0 1 2.11-.45 12.84 12.84 0 0 0 2.81.7A2 2 0 0 1 22 16.92z"/>
					</svg>
				</div>
				<h3>Call Us</h3>
				<p>+91 81999 33902<br/>Mon-Fri 4pm - 6pm IST</p>
			</div>

			<div class="info-card">
				<div class="icon-wrapper">
					<svg width="28" height="28" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
						<path d="M4 4h16c1.1 0 2 .9 2 2v12c0 1.1-.9 2-2 2H4c-1.1 0-2-.9-2-2V6c0-1.1.9-2 2-2z"/>
						<polyline points="22,6 12,13 2,6"/>
					</svg>
				</div>
				<h3>Email Us</h3>
				<p><a href="mailto:yakshgoel090@gmail.com">yakshgoel090@gmail.com</a><br/>We'll respond within 48 hours</p>
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

	.contact-container {
		display: flex;
		justify-content: center;
		max-width: 800px;
		margin: 0 auto;
	}

	.info-section-full {
		display: flex;
		flex-direction: column;
		gap: 2rem;
		width: 100%;
	}

	.info-card {
		background: white;
		padding: 2rem;
		border-radius: 20px;
		box-shadow: 0 10px 40px rgba(0, 153, 77, 0.1);
		border: 2px solid transparent;
		transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
		position: relative;
		overflow: hidden;
	}

	.info-card::before {
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

	.info-card:hover {
		transform: translateX(5px);
		box-shadow: 0 20px 60px rgba(0, 153, 77, 0.2);
		border-color: #00994d;
	}

	.icon-wrapper {
		width: 60px;
		height: 60px;
		background: linear-gradient(135deg, rgba(0, 153, 77, 0.1), rgba(0, 204, 102, 0.1));
		border-radius: 15px;
		display: flex;
		align-items: center;
		justify-content: center;
		margin-bottom: 1rem;
		color: #00994d;
		transition: all 0.3s;
	}

	.info-card:hover .icon-wrapper {
		background: linear-gradient(135deg, #00994d, #00cc66);
		color: white;
		transform: scale(1.1);
	}

	.info-card h3 {
		font-size: 1.3rem;
		font-weight: 600;
		color: #333;
		margin-bottom: 0.8rem;
		transition: all 0.3s;
	}

	.info-card:hover h3 {
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
	}

	.info-card p {
		color: #666;
		line-height: 1.8;
		font-size: 0.95rem;
		margin: 0;
	}

	.info-card p a {
		color: #00994d;
		text-decoration: none;
		font-weight: 500;
		transition: all 0.3s;
	}

	.info-card p a:hover {
		text-decoration: underline;
	}

	@media (max-width: 968px) {

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

		.info-card {
			padding: 1.5rem;
		}
	}
</style>