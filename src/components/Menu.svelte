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
		{ label: 'Sobre', href: '#sobre' },
		{ label: 'Serviços', href: '#servicos' },
		{ label: 'Galeria', href: '#galeria' },
		{ label: 'Depoimentos', href: '#depoimentos' },
		{ label: 'Contato', href: '#contato' }
	];
</script>

<nav class="nav">
	<div class="logo-wrapper">
		<a href="#inicio" class="logo-link" onclick={closeMenu}>
			<img class="logo" src="/logo.png" alt="Logo da Clínica" />
		</a>
		<h1 class="logo-text">Unitá Estética</h1>
	</div>

	<button class="menu-toggle" onclick={toggleMenu} aria-label="Abrir menu">
		<span class="hamburger" class:open={isMenuOpen}></span>
	</button>

	<!-- container que só serve para o mobile -->
	<div class="menu-wrapper" class:open={isMenuOpen}>
		<ul class="menu">
			{#each menuItems as item}
				<li class="menu-item">
					<a href={item.href} class="menu-link" onclick={closeMenu}>
						{item.label}
					</a>
				</li>
			{/each}
				<a class="btn-primary" href="https://wa.me/5586998678703?text={encodeURIComponent("Olá, gostaria de agendar uma consulta!")}" target="_blank" >
					Agendar Consulta
				</a>
		</ul>
	</div>
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

.logo-wrapper {
	align-items: center;
	display: flex;
}

.logo-text {
	color: var(--secondary);
	font-family: var(--font-primary);
	font-size: 20px;
	margin-left: 16px;
}

.logo-link {
	align-items: center;
	background: #f9f9fa;
	border-radius: 999px;
	display: flex;
	padding: 8px;
	z-index: 15;
}

.logo {
	height: 40px;
	width: auto;
}

.menu-toggle {
	display: flex;
	justify-content: center;
	align-items: center;
	width: 40px;
	height: 40px;
	z-index: 1002;
	cursor: pointer;
}

/* hamburguer */
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

/* ===== Mobile Menu ===== */
.menu-wrapper {
	position: fixed;
	top: 0;
	right: 0;
	width: 280px;
	height: 100vh;
	background: linear-gradient(135deg, var(--tertiary) 0%, rgba(255, 255, 255, 0.98) 100%);
	box-shadow: -5px 0 20px rgba(0, 0, 0, 0.1);
	padding: 2rem;
	transform: translateX(100%); /* começa fora */
	transition: transform 0.3s ease;
	z-index: 1000;

	display: flex;
	flex-direction: column;
	align-items: center;
	justify-content: center;

	&.open {
		transform: translateX(0);
	}
}

.menu {
	display: flex;
	flex-direction: column;
	gap: 2rem;
	list-style: none;
	align-items: center;
	padding: 0;
	margin: 0;
	width: 100%;
}

.menu-link {
	font-family: var(--font-tertiary);
	font-size: 1.1rem;
	color: var(--secondary);
	text-decoration: none;
	padding: 0.5rem 0;
	position: relative;
	transition: color 0.3s ease;

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

	&:hover::after {
		width: 100%;
	}
}

.menu-cta {
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
	margin-top: 2rem;

	&:hover {
		transform: translateY(-2px);
		box-shadow: 0 6px 20px rgba(0, 64, 60, 0.3);
	}
}

/* ===== Desktop overrides ===== */
@media (min-width: 969px) {

	.logo-text {
		display: none;
	}

	.menu-toggle {
		display: none;
	}

	.menu-wrapper {
		position: static;
		transform: none;
		box-shadow: none;
		background: transparent;
		height: auto;
		width: auto;
		padding: 0;
	}

	.menu {
		flex-direction: row;
		gap: 2.5rem;
	}

	.menu-cta {
		margin-top: 0;
	}
}

	.btn-primary {
		align-items: center;
		display: flex;
		font-family: var(--font-tertiary);
		font-weight: 500;
		font-size: 14px;
		padding: 1rem 2rem;
		border-radius: 30px;
		text-decoration: none;
		transition: all 0.3s ease;
		width: 100%;
		max-width: 280px;
		text-align: center;
		background-color: var(--secondary);
		color: var(--on-surface);
		box-shadow: 0 4px 15px rgba(0, 64, 60, 0.3);

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 6px 20px rgba(0, 64, 60, 0.4);
		}
	}
</style>
