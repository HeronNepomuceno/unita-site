<script lang="ts">
	let isMenuOpen = $state(false);

	function toggleMenu() {
		isMenuOpen = !isMenuOpen;
	}

	function closeMenu() {
		isMenuOpen = false;
	}

	const menuItems = [
		{ label: 'Início', href: '#inicio' },
		{ label: 'Serviços', href: '#servicos' },
		{ label: 'Sobre', href: '#sobre' },
		{ label: 'Galeria', href: '#galeria' },
		{ label: 'Depoimentos', href: '#depoimentos' },
		{ label: 'Contato', href: '#contato' }
	];
</script>

<nav class="nav">
	<button class="logo-link" onclick={closeMenu}>
		<img class="logo" src="/unita.png" alt="Logo da Clínica"  />
	</button>

	<button class="menu-toggle" onclick={toggleMenu} aria-label="Toggle menu">
		<span class="hamburger" class:open={isMenuOpen}></span>
	</button>

	<ul class="menu" class:open={isMenuOpen}>
		{#each menuItems as item}
			<li class="menu-item">
				<a href={item.href} class="menu-link" onclick={closeMenu}>
					{item.label}
				</a>
			</li>
		{/each}
	</ul>

	<a href="#agendamento" class="menu-cta" onclick={closeMenu}>
		Agendar consulta
	</a>
</nav>

<style lang="scss">
	.nav {
		display: flex;
		align-items: center;
		justify-content: space-between;
		padding: 1rem 1.5rem;
		max-width: 1400px;
		margin: 0 auto;
		width: 100%;
	}

	.logo-link {
		display: flex;
		align-items: center;
		z-index: 1001;
		background: #f9f9fa;
	}

	.logo {
		height: 40px;
		width: auto;
		object-fit:unset;
	}

	.menu-toggle {
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		width: 40px;
		height: 40px;
		z-index: 1001;
		cursor: pointer;
	}

	.hamburger {
		position: relative;
		width: 26px;
		height: 2px;
		background-color: var(--secondary);
		transition: all 0.3s ease;

		&::before,
		&::after {
			content: '';
			position: absolute;
			width: 26px;
			height: 2px;
			background-color: var(--secondary);
			transition: all 0.3s ease;
		}

		&::before {
			transform: translateY(-8px);
		}

		&::after {
			transform: translateY(8px);
		}

		&.open {
			background-color: transparent;

			&::before {
				transform: rotate(45deg);
			}

			&::after {
				transform: rotate(-45deg);
			}
		}
	}

	.menu {
		position: fixed;
		top: 0;
		right: -100%;
		width: 280px;
		height: 100vh;
		display: flex;
		flex-direction: column;
		justify-content: center;
		align-items: center;
		gap: 2rem;
		list-style: none;
		background: linear-gradient(135deg, var(--tertiary) 0%, rgba(255, 255, 255, 0.98) 100%);
		box-shadow: -5px 0 20px rgba(0, 0, 0, 0.1);
		transition: right 0.4s cubic-bezier(0.68, -0.55, 0.265, 1.55);
		padding: 2rem;

		&.open {
			right: 0;
		}
	}

	.menu-item {
		list-style: none;
	}

	.menu-link {
		font-family: var(--font-tertiary);
		font-size: 1.1rem;
		color: var(--secondary);
		text-decoration: none;
		position: relative;
		transition: color 0.3s ease;
		padding: 0.5rem 0;

		&::after {
			content: '';
			position: absolute;
			bottom: 0;
			left: 0;
			width: 0;
			height: 2px;
			background-color: var(--secondary);
			transition: width 0.3s ease;
		}

		&:hover {
			&::after {
				width: 100%;
			}
		}
	}

	.menu-cta {
		display: none;
		font-family: var(--font-tertiary);
		font-weight: 500;
		font-size: 1rem;
		color: var(--on-surface);
		background-color: var(--secondary);
		padding: 1rem 2rem;
		border-radius: 30px;
		text-decoration: none;
		transition: all 0.3s ease;
		box-shadow: 0 4px 15px rgba(203, 146, 118, 0.3);
		margin-top: 1rem;

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 6px 20px rgba(0, 64, 60, 0.3);
		}
	}

	// Tablet
	@media (min-width: 768px) {
		.logo {
			height: 45px;
		}
	}

	// Desktop
	@media (min-width: 969px) {
		.nav {
			padding: 1.2rem 2rem;
		}

		.logo {
			height: 50px;
		}

		.menu-toggle {
			display: none;
		}

		.menu {
			position: static;
			width: auto;
			height: auto;
			flex-direction: row;
			gap: 2.5rem;
			background: transparent;
			box-shadow: none;
			padding: 0;
			transition: none;
		}

		.menu-link {
			font-size: 1rem;
		}

		.menu-cta {
			display: block;
			font-size: 0.95rem;
			padding: 0.8rem 1.8rem;
			margin-top: 0;
		}
	}
</style>