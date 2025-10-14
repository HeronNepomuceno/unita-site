<script lang="ts">
	const currentYear = new Date().getFullYear();

	const quickLinks = [
		{ label: 'Início', href: '#inicio' },
		{ label: 'Sobre', href: '#sobre' },
		{ label: 'Serviços', href: '#servicos' },
		{ label: 'Galeria', href: '#galeria' },
		{ label: 'Depoimentos', href: '#depoimentos' },
		{ label: 'Contato', href: '#contato' }
	];

	const services = [
		{ label: 'Harmonização Facial', href: '#servicos' },
		{ label: 'Tratamentos Corporais', href: '#servicos' },
		{ label: 'Skincare Premium', href: '#servicos' },
		{ label: 'Bem-estar Integral', href: '#servicos' }
	];

	const socialMedia = [
		{ name: 'Instagram', icon: '📷', href: '#' },
		{ name: 'Facebook', icon: '📘', href: '#' },
		{ name: 'WhatsApp', icon: '💬', href: '#' }
	];
</script>

<footer class="footer">
	<div class="footer-content">

		<!-- Links Rápidos -->
		<div class="footer-section">
			<h3 class="footer-title">Links Rápidos</h3>
			<ul class="footer-links">
				{#each quickLinks as link}
					<li>
						<a href={link.href} class="footer-link">{link.label}</a>
					</li>
				{/each}
			</ul>
		</div>

		<!-- Serviços -->
		<div class="footer-section">
			<h3 class="footer-title">Serviços</h3>
			<ul class="footer-links">
				{#each services as service}
					<li>
						<a href={service.href} class="footer-link">{service.label}</a>
					</li>
				{/each}
			</ul>
		</div>

		<!-- Contato -->
		<div class="footer-section">
			<h3 class="footer-title">Contato</h3>
			<div class="footer-contact">
				<div class="contact-item">
					<span class="contact-icon">📍</span>
					<span>Avenida Senador Area Leão, 1736 sala 4 - Zona Leste - Bairro Jóquei</span>
				</div>
				<div class="contact-item">
					<span class="contact-icon">📞</span>
					<span>+55 (86) 99867-8703</span>
				</div>
				<div class="contact-item">
					<span class="contact-icon">📧</span>
					<span>unita.the@gmail.com</span>
				</div>
				<div class="contact-item">
					<span class="contact-icon">🕐</span>
					<span>Seg. a sex.: 9h às 18h · Sáb.: 9h às 13h</span>
				</div>
			</div>
		</div>
	</div>

	<!-- Copyright -->
	<div class="footer-bottom">
		<p class="copyright">
			© {currentYear} Unitá Estética e Saúde Integrativa. Todos os direitos reservados.
		</p>
		<div class="footer-legal">
			<a href="#privacidade" class="legal-link">Política de Privacidade</a>
			<span class="separator">•</span>
			<a href="#termos" class="legal-link">Termos de Uso</a>
		</div>
	</div>
</footer>

<style lang="scss">
	.footer {
		background: linear-gradient(135deg, var(--secondary) 0%, rgba(0, 64, 60, 0.95) 100%);
		color: var(--on-surface);
		padding: 3rem 1.5rem 1.5rem;
		margin-top: 4rem;
	}

	.footer-content {
		max-width: 1400px;
		margin: 0 auto;
		display: grid;
		gap: 2.5rem;
		margin-bottom: 2.5rem;

		/* Mobile: 1 coluna */
		grid-template-columns: 1fr;
	}

	.footer-section {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.footer-title {
		font-family: var(--font-primary);
		font-size: 1.3rem;
		margin-bottom: 0.5rem;
		color: var(--tertiary);
	}

	.footer-links {
		list-style: none;
		display: flex;
		flex-direction: column;
		gap: 0.8rem;
	}

	.footer-link {
		font-family: var(--font-tertiary);
		font-size: 0.95rem;
		color: var(--on-surface);
		text-decoration: none;
		opacity: 0.85;
		transition: all 0.3s ease;
		display: inline-block;
		position: relative;

		&::after {
			content: '';
			position: absolute;
			bottom: -2px;
			left: 0;
			width: 0;
			height: 1px;
			background-color: var(--primary);
			transition: width 0.3s ease;
		}

		&:hover {
			opacity: 1;
			color: var(--primary);
			transform: translateX(5px);

			&::after {
				width: 100%;
			}
		}
	}

	.footer-contact {
		display: flex;
		flex-direction: column;
		gap: 1rem;
	}

	.contact-item {
		font-family: var(--font-tertiary);
		font-size: 0.9rem;
		display: flex;
		align-items: flex-start;
		gap: 0.8rem;
		opacity: 0.9;
		line-height: 1.5;
	}

	.contact-icon {
		font-size: 1.2rem;
		flex-shrink: 0;
	}

	.footer-bottom {
		max-width: 1400px;
		margin: 0 auto;
		padding-top: 2rem;
		border-top: 1px solid rgba(255, 255, 255, 0.1);
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 1rem;
		text-align: center;
	}

	.copyright {
		font-family: var(--font-tertiary);
		font-size: 0.85rem;
		opacity: 0.7;
	}

	.footer-legal {
		display: flex;
		align-items: center;
		gap: 0.8rem;
		flex-wrap: wrap;
		justify-content: center;
	}

	.legal-link {
		font-family: var(--font-tertiary);
		font-size: 0.85rem;
		color: var(--on-surface);
		text-decoration: none;
		opacity: 0.7;
		transition: all 0.3s ease;

		&:hover {
			opacity: 1;
			color: var(--primary);
		}
	}

	.separator {
		opacity: 0.5;
		font-size: 0.85rem;
	}

	// Tablet
	@media (min-width: 768px) {
		.footer {
			padding: 4rem 2rem 2rem;
		}

		.footer-content {
			grid-template-columns: repeat(2, 1fr); /* 2 colunas */
			gap: 3rem;
		}

		.footer-bottom {
			flex-direction: row;
			justify-content: space-between;
			text-align: left;
		}

		.footer-legal {
			justify-content: flex-end;
		}
	}

	// Desktop
	@media (min-width: 969px) {
		.footer {
			padding: 5rem 2rem 2rem;
		}

		.footer-content {
			grid-template-columns: 1fr 1fr 1.5fr; /* 3 colunas: links | serviços | contato */
			gap: 4rem;
		}

		.footer-title {
			font-size: 1.4rem;
		}
	}
</style>