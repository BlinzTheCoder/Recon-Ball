<script lang="ts">
	import './layout.css';
	import { goto } from '$app/navigation';
	import favicon from '$lib/assets/favicon.svg';

	let { children } = $props();

	const Navbar = [
		{ name: 'Home', href: '/' },
		{ name: 'Features', href: '/features' },
		{ name: 'Team', href: '/team' },
		{ name: 'Contact', href: '/contact' }
	];

	function gotopage(page: string) {
		goto(page);
	}
</script>

<nav>
	<div class="logo">
		<div class="logo-icon">
			<svg width="32" height="32" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2.5">
				<!-- Grenade body -->
				<ellipse cx="12" cy="14" rx="5" ry="6"/>
				<!-- Pin ring -->
				<circle cx="12" cy="6" r="1.5"/>
				<!-- Pin -->
				<path d="M12 4.5V7.5"/>
				<!-- Lever -->
				<path d="M14 7C15 6.5 16 6 16 4.5"/>
				<!-- Bottom bumps -->
				<line x1="9" y1="20" x2="9" y2="20.5"/>
				<line x1="12" y1="20.5" x2="12" y2="21"/>
				<line x1="15" y1="20" x2="15" y2="20.5"/>
			</svg>
		</div>
		<span class="logo-text">Recon Ball</span>
	</div>
	
	<div class="nav-items">
		{#each Navbar as item}
			<div class="nav-item">
				<button class="nav-button" onclick={() => gotopage(item.href)}>
					{item.name}
				</button>
			</div>
		{/each}
	</div>
</nav>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

{@render children()}

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');

	:global(body) {
		margin: 0;
		padding: 0;
		font-family: 'Poppins', sans-serif;
	}

	nav {
		width: 100vw;
		height: 70px;
		background: white;
		display: flex;
		justify-content: space-between;
		align-items: center;
		gap: 3rem;
		padding: 0 3rem;
		position: sticky;
		top: 0;
		z-index: 1000;
		box-shadow: 0 2px 20px rgba(0, 153, 77, 0.08);
		border-bottom: 2px solid rgba(0, 153, 77, 0.1);
	}

	.logo {
		display: flex;
		align-items: center;
		gap: 0.8rem;
		cursor: pointer;
		transition: all 0.3s;
	}

	.logo:hover {
		transform: translateX(5px);
	}

	.logo-icon {
		width: 40px;
		height: 40px;
		background: linear-gradient(135deg, #00994d, #00cc66);
		border-radius: 10px;
		display: flex;
		align-items: center;
		justify-content: center;
		color: white;
		box-shadow: 0 4px 12px rgba(0, 153, 77, 0.3);
		transition: all 0.3s;
	}

	.logo:hover .logo-icon {
		transform: rotate(10deg);
		box-shadow: 0 6px 16px rgba(0, 153, 77, 0.4);
	}

	.logo-text {
		font-size: 1.4rem;
		font-weight: 700;
		background: linear-gradient(135deg, #00994d, #00cc66);
		-webkit-background-clip: text;
		-webkit-text-fill-color: transparent;
		background-clip: text;
		letter-spacing: -0.5px;
	}

	.nav-items {
		display: flex;
		gap: 0.5rem;
	}

	.nav-item {
		font-size: 1rem;
		font-family: 'Poppins', sans-serif;
		font-weight: 500;
	}
	
	.nav-button {
		padding: 0.7rem 1.2rem;
		border-radius: 8px;
		transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
		color: #333;
		background: transparent;
		border: none;
		font-family: 'Poppins', sans-serif;
		font-size: 1rem;
		font-weight: 500;
		cursor: pointer;
		position: relative;
		overflow: hidden;
	}

	.nav-button::before {
		content: '';
		position: absolute;
		bottom: 0;
		left: 50%;
		width: 0;
		height: 2px;
		background: linear-gradient(90deg, #00994d, #00cc66);
		transition: all 0.3s;
		transform: translateX(-50%);
	}

	.nav-button:hover {
		background-color: rgba(0, 153, 77, 0.08);
		color: #00994d;
		transform: translateY(-2px);
	}

	.nav-button:hover::before {
		width: 80%;
	}

	.cta-nav {
		padding: 0.7rem 1.5rem;
		background: linear-gradient(135deg, #00994d, #00cc66);
		color: white;
		border: none;
		border-radius: 25px;
		font-family: 'Poppins', sans-serif;
		font-size: 0.95rem;
		font-weight: 600;
		cursor: pointer;
		display: flex;
		align-items: center;
		gap: 0.5rem;
		transition: all 0.3s;
		box-shadow: 0 4px 12px rgba(0, 153, 77, 0.3);
	}

	.cta-nav:hover {
		transform: translateY(-2px);
		box-shadow: 0 6px 20px rgba(0, 153, 77, 0.4);
		background: linear-gradient(135deg, #00cc66, #00994d);
	}

	.cta-nav:active {
		transform: translateY(0);
	}

	.cta-nav svg {
		transition: transform 0.3s;
	}

	.cta-nav:hover svg {
		transform: translateX(3px);
	}

	@media (max-width: 768px) {
		nav {
			padding: 0 1.5rem;
			height: auto;
			min-height: 70px;
			flex-wrap: wrap;
			justify-content: center;
			gap: 1rem;
			padding-top: 1rem;
			padding-bottom: 1rem;
		}

		.nav-items {
			width: 100%;
			justify-content: center;
			gap: 0.3rem;
			flex-wrap: wrap;
		}

		.nav-button {
			padding: 0.5rem 1rem;
			font-size: 0.9rem;
		}
	}
</style>