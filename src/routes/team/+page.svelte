<script lang="ts">
	import Footer from '$lib/components/Footer.svelte';
</script>

<main>
	<div class="section-header">
		<h1 class="title">Our Team</h1>
		<div class="divider"></div>
		<p class="subtitle">Meet the innovators behind Recon Ball</p>
	</div>

	<div class="row">
		<div class="item">
			<div class="avatar">SK</div>
			<h2>Sahasanu Karthick</h2>
			<p class="role">Team Leader</p>
			<p class="description">Project Leader, Research, Documentation, Designed Models for project presentation</p>
		</div>
		<div class="item">
			<div class="avatar">AA</div>
			<h2>Arjun Ahuja</h2>
			<p class="role">Co-Leader</p>
			<p class="description">Coding & Wireless Systems, Trained AI</p>
		</div>
	</div>
	<div class="row">
		<div class="item">
			<div class="avatar">YG</div>
			<h2>Yaksh Goel</h2>
			<p class="role">Designer</p>
			<p class="description">Miscellaneous Work, Project Presentation, Website, Reasearch</p>
		</div>
		<div class="item">
			<div class="avatar">SG</div>
			<h2>Satvik Gupta</h2>
			<p class="role">Lead Designer</p>
			<p class="description">Outer Shell 3D Model, Designed Models for project presentation</p>
		</div>
	</div>
</main>
<Footer />

<style>
	.section-header {
		text-align: center;
		margin-top: 2rem;
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

	.row {
		display: flex;
		justify-content: center;
		gap: 3rem;
		margin-bottom: 3rem;
	}

	.item {
		text-align: center;
		background: white;
		padding: 2.5rem;
		border-radius: 20px;
		flex: 1;
		max-width: 400px;
		box-shadow: 0 10px 40px rgba(0, 153, 77, 0.1);
		transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
		border: 2px solid transparent;
		position: relative;
		overflow: hidden;
	}

	.item::before {
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

	.item:hover {
		transform: translateY(-10px);
		box-shadow: 0 20px 60px rgba(0, 153, 77, 0.2);
		border-color: #00994d;
	}

	.avatar {
		width: 100px;
		height: 100px;
		margin: 0 auto 1.5rem;
		background: linear-gradient(135deg, #00994d, #00cc66);
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		font-size: 2rem;
		font-weight: 700;
		box-shadow: 0 8px 24px rgba(0, 153, 77, 0.3);
		transition: all 0.3s;
	}

	.item:hover .avatar {
		transform: scale(1.1);
		box-shadow: 0 12px 32px rgba(0, 153, 77, 0.4);
	}

	.item h2 {
		font-size: 1.5rem;
		font-weight: 600;
		color: #333;
		margin: 1rem 0 0.5rem;
		transition: all 0.3s;
	}

	.item:hover h2 {
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
	}

	.role {
		font-size: 1rem;
		font-weight: 500;
		color: #00994d;
		margin: 0.5rem 0;
		text-transform: uppercase;
		letter-spacing: 1px;
		font-size: 0.85rem;
	}

	.description {
		font-size: 0.95rem;
		color: #666;
		line-height: 1.6;
		margin: 1rem 0 0;
	}

	@media (max-width: 968px) {
		.row {
			flex-direction: column;
			gap: 2rem;
		}

		.item {
			max-width: 100%;
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

		.item {
			padding: 2rem 1.5rem;
		}

		.avatar {
			width: 80px;
			height: 80px;
			font-size: 1.5rem;
		}
	}
</style>
