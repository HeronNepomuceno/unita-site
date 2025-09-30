<script lang="ts">
	
	const services = [
		{
			title: 'Depilação a laser',
			description: 'Tecnologia avançada para remoção definitiva de pelos',
			icon: '✨'
		},
		{
			title: 'Redução de medidas',
			description: 'Tratamentos eficazes para modelagem corporal',
			icon: '📏'
		},
		{
			title: 'Limpeza de pele',
			description: 'Cuidado profundo para uma pele saudável e radiante',
			icon: '🌸'
		},
		{
			title: 'Microagulhamento',
			description: 'Estímulo natural do colágeno para rejuvenescimento',
			icon: '💉'
		},
		{
			title: 'Massagem relaxante',
			description: 'Alívio do estresse e tensões musculares',
			icon: '💆'
		},
		{
			title: 'Drenagem linfática',
			description: 'Eliminação de toxinas e redução de inchaços',
			icon: '🌊'
		},
		{
			title: 'Massagem modeladora',
			description: 'Modelagem corporal e combate à celulite',
			icon: '🙌'
		},
		{
			title: 'Acupuntura',
			description: 'Equilíbrio energético através da medicina tradicional',
			icon: '🎯'
		},
		{
			title: 'Reiki',
			description: 'Terapia energética para harmonização do corpo e mente',
			icon: '🧘'
		},
		{
			title: 'Ventosaterapia',
			description: 'Técnica milenar para alívio de dores e tensões',
			icon: '⭕'
		},
		{
			title: 'Detox corporal',
			description: 'Limpeza profunda e revitalização do organismo',
			icon: '🍃'
		},
		{
			title: 'Secagem de vasinhos',
			description: 'Tratamento para vasos e microvarizes',
			icon: '💜'
		},
		{
			title: 'Botox',
			description: 'Suavização de rugas e linhas de expressão',
			icon: '💫'
		},
		{
			title: 'Rejuvenescimento facial',
			description: 'Protocolos para renovação e vitalidade da pele',
			icon: '✨'
		},
		{
			title: 'Harmonização corporal',
			description: 'Procedimentos para contorno e simetria corporal',
			icon: '👤'
		},
		{
			title: 'Clareamento íntimo',
			description: 'Tratamento delicado para áreas sensíveis',
			icon: '🌺'
		}
	];

	const testimonials = [
		{
			name: 'Maria Silva',
			text: 'Profissionais incríveis! Me senti acolhida e os resultados superaram minhas expectativas.',
			rating: 5
		},
		{
			name: 'Ana Paula',
			text: 'A clínica é maravilhosa, ambiente tranquilo e tratamentos de altíssima qualidade.',
			rating: 5
		},
		{
			name: 'Juliana Costa',
			text: 'Melhor experiência! Equipe atenciosa e resultados naturais e incríveis.',
			rating: 5
		}
	];
</script>

<div class="page">
	<!-- Hero Section -->
	<section id="inicio" class="hero">
		<div class="hero-content">
			<h1 class="hero-title">
				Desperte sua
				<span class="highlight">beleza natural</span>
			</h1>
			<p class="hero-subtitle">
				Clínica de estética facial, corporal e terapias integrativas.
			</p>
			<div class="hero-actions">
				<a href="#agendamento" class="btn-primary">Agendar Consulta</a>
				<a href="#servicos" class="btn-secondary">Nossos Serviços</a>
			</div>
		</div>
		<div class="hero-image">
			<div class="image-placeholder">
				<span>🌿</span>
			</div>
		</div>
	</section>

		<!-- About Section -->
	<section id="sobre" class="about">
		<div class="about-content">
			<h2 class="section-title">Sobre a Unitá</h2>
			<p class="about-text">
				Somos uma clínica dedicada à estética integrativa, combinando tecnologia de ponta com
				abordagens holísticas para proporcionar resultados naturais e duradouros.
			</p>
			<p class="about-text">
				Nossa missão é despertar a melhor versão de você, respeitando sua individualidade e
				promovendo saúde, autoestima e bem-estar.
			</p>
			<div class="about-stats">
				<div class="stat">
					<div class="stat-number">10+</div>
					<div class="stat-label">Anos de experiência</div>
				</div>
				<div class="stat">
					<div class="stat-number">5000+</div>
					<div class="stat-label">Clientes satisfeitos</div>
				</div>
				<div class="stat">
					<div class="stat-number">98%</div>
					<div class="stat-label">Taxa de aprovação</div>
				</div>
			</div>
		</div>
		<div class="about-image">
			<div class="image-placeholder">
				<span>💎</span>
			</div>
		</div>
	</section>

	<!-- Services Section -->
	<section id="servicos" class="services">
		<div class="section-header">
			<h2 class="section-title">Nossos Serviços</h2>
			<p class="section-subtitle">Cuidado personalizado para cada necessidade</p>
		</div>

		<div class="services-grid">
			{#each services as service}
				<div class="service-card">
					<div class="service-icon">{service.icon}</div>
					<h3 class="service-title">{service.title}</h3>
					<p class="service-description">{service.description}</p>
				</div>
			{/each}
		</div>
	</section>

	<!-- Gallery Section -->
	<section id="galeria" class="gallery">
		<div class="section-header">
			<h2 class="section-title">Galeria</h2>
			<p class="section-subtitle">Confira alguns dos nossos trabalhos</p>
		</div>

		<div class="gallery-grid">
			{#each Array(6) as _, i}
				<div class="gallery-item">
					<div class="gallery-placeholder">
						<span>📸</span>
					</div>
				</div>
			{/each}
		</div>
	</section>

	<!-- Testimonials Section -->
	<section id="depoimentos" class="testimonials">
		<div class="section-header">
			<h2 class="section-title">Depoimentos</h2>
			<p class="section-subtitle">O que nossos clientes dizem</p>
		</div>

		<div class="testimonials-grid">
			{#each testimonials as testimonial}
				<div class="testimonial-card">
					<div class="testimonial-stars">
						{#each Array(testimonial.rating) as _}
							<span class="star">⭐</span>
						{/each}
					</div>
					<p class="testimonial-text">"{testimonial.text}"</p>
					<p class="testimonial-author">— {testimonial.name}</p>
				</div>
			{/each}
		</div>
	</section>

	<!-- Contact Section -->
	<section id="contato" class="contact">
		<div class="contact-content">
			<h2 class="section-title">Entre em Contato</h2>
			<p class="section-subtitle">Estamos prontos para atender você</p>

			<div class="contact-info">
				<div class="contact-item">
					<span class="contact-icon">📍</span>
					<div>
						<h4>Endereço</h4>
						<p>Rua Principal, 123 - Centro</p>
					</div>
				</div>
				<div class="contact-item">
					<span class="contact-icon">📞</span>
					<div>
						<h4>Telefone</h4>
						<p>(86) 99999-9999</p>
					</div>
				</div>
				<div class="contact-item">
					<span class="contact-icon">📧</span>
					<div>
						<h4>Email</h4>
						<p>contato@unita.com.br</p>
					</div>
				</div>
				<div class="contact-item">
					<span class="contact-icon">🕐</span>
					<div>
						<h4>Horário</h4>
						<p>Seg - Sex: 8h às 18h</p>
					</div>
				</div>
			</div>
		</div>
	</section>
</div>

<style lang="scss">
	.page {
		width: 100%;
		max-width: 100%;
		overflow-x: hidden;
	}

	// Hero Section
	.hero {
		min-height: calc(100vh - 160px);
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
		padding: 2rem 1.5rem;
		gap: 2rem;
	}

	.hero-content {
		text-align: center;
		max-width: 600px;
	}

	.hero-title {
		font-family: var(--font-primary);
		font-size: 2.5rem;
		line-height: 1.2;
		color: var(--secondary);
		margin-bottom: 1rem;

		.highlight {
			color: var(--primary);
			display: block;
		}
	}

	.hero-subtitle {
		font-family: var(--font-tertiary);
		font-size: 1rem;
		line-height: 1.6;
		color: var(--secondary);
		opacity: 0.8;
		margin-bottom: 2rem;
	}

	.hero-actions {
		display: flex;
		flex-direction: column;
		gap: 1rem;
		align-items: center;
	}

	.btn-primary,
	.btn-secondary {
		font-family: var(--font-tertiary);
		font-weight: 500;
		padding: 1rem 2rem;
		border-radius: 30px;
		text-decoration: none;
		transition: all 0.3s ease;
		width: 100%;
		max-width: 280px;
		text-align: center;
	}

	.btn-primary {
		background-color: var(--secondary);
		color: var(--on-surface);
		box-shadow: 0 4px 15px rgba(0, 64, 60, 0.3);

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 6px 20px rgba(0, 64, 60, 0.4);
		}
	}

	.btn-secondary {
		background-color: transparent;
		color: var(--secondary);
		border: 2px solid var(--secondary);

		&:hover {
			background-color: var(--secondary);
			color: var(--on-surface);
		}
	}

	.hero-image {
		width: 100%;
		max-width: 400px;
	}

	.image-placeholder {
		aspect-ratio: 1;
		background: linear-gradient(135deg, var(--primary), var(--tertiary));
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 5rem;
		box-shadow: 0 10px 40px rgba(203, 146, 118, 0.3);
	}

	// Section Shared Styles
	section {
		padding: 3rem 1.5rem;
	}

	.section-header {
		text-align: center;
		margin-bottom: 2.5rem;
	}

	.section-title {
		font-family: var(--font-primary);
		font-size: 2rem;
		color: var(--secondary);
		margin-bottom: 0.5rem;
	}

	.section-subtitle {
		font-family: var(--font-tertiary);
		color: var(--secondary);
		opacity: 0.7;
	}

	// Services Section
	.services-grid {
		display: grid;
		gap: 1.5rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.service-card {
		background: white;
		padding: 2rem;
		border-radius: 20px;
		box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
		transition: transform 0.3s ease, box-shadow 0.3s ease;

		&:hover {
			transform: translateY(-5px);
			box-shadow: 0 10px 30px rgba(0, 0, 0, 0.1);
		}
	}

	.service-icon {
		font-size: 3rem;
		margin-bottom: 1rem;
	}

	.service-title {
		font-family: var(--font-primary);
		font-size: 1.3rem;
		color: var(--secondary);
		margin-bottom: 0.5rem;
	}

	.service-description {
		font-family: var(--font-tertiary);
		color: var(--secondary);
		opacity: 0.7;
		line-height: 1.6;
		margin-bottom: 1rem;
	}

	.service-link {
		font-family: var(--font-tertiary);
		color: var(--primary);
		font-weight: 500;
		text-decoration: none;
		display: inline-block;
		transition: transform 0.3s ease;

		&:hover {
			transform: translateX(5px);
		}
	}

	// About Section
	.about {
		background: rgba(255, 255, 255, 0.5);
		display: flex;
		flex-direction: column;
		gap: 2rem;
		align-items: center;
	}

	.about-content {
		max-width: 600px;
	}

	.about-text {
		font-family: var(--font-tertiary);
		color: var(--secondary);
		line-height: 1.8;
		margin-bottom: 1.5rem;
	}

	.about-stats {
		display: grid;
		grid-template-columns: repeat(3, 1fr);
		gap: 1rem;
		margin-top: 2rem;
	}

	.stat {
		text-align: center;
		padding: 1rem;
		background: white;
		border-radius: 15px;
		box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
	}

	.stat-number {
		font-family: var(--font-primary);
		font-size: 1.8rem;
		color: var(--primary);
		font-weight: bold;
	}

	.stat-label {
		font-family: var(--font-tertiary);
		font-size: 0.75rem;
		color: var(--secondary);
		opacity: 0.7;
		margin-top: 0.3rem;
	}

	.about-image {
		width: 100%;
		max-width: 400px;
	}

	// Gallery Section
	.gallery {
		background: rgba(255, 255, 255, 0.5);
	}

	.gallery-grid {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 1rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.gallery-item {
		aspect-ratio: 1;
		overflow: hidden;
		border-radius: 15px;
	}

	.gallery-placeholder {
		width: 100%;
		height: 100%;
		background: linear-gradient(135deg, var(--tertiary), var(--primary));
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 3rem;
		transition: transform 0.3s ease;

		&:hover {
			transform: scale(1.05);
		}
	}

	// Testimonials Section
	.testimonials-grid {
		display: grid;
		gap: 1.5rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.testimonial-card {
		background: white;
		padding: 2rem;
		border-radius: 20px;
		box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
	}

	.testimonial-stars {
		margin-bottom: 1rem;
	}

	.star {
		font-size: 1.2rem;
	}

	.testimonial-text {
		font-family: var(--font-tertiary);
		color: var(--secondary);
		line-height: 1.6;
		margin-bottom: 1rem;
		font-style: italic;
	}

	.testimonial-author {
		font-family: var(--font-tertiary);
		color: var(--primary);
		font-weight: 500;
	}

	// Contact Section
	.contact {
		background: rgba(255, 255, 255, 0.5);
	}

	.contact-content {
		max-width: 800px;
		margin: 0 auto;
	}

	.contact-info {
		display: grid;
		gap: 1.5rem;
		margin-top: 2rem;
	}

	.contact-item {
		display: flex;
		gap: 1rem;
		padding: 1.5rem;
		background: white;
		border-radius: 15px;
		box-shadow: 0 5px 15px rgba(0, 0, 0, 0.05);
	}

	.contact-icon {
		font-size: 2rem;
	}

	.contact-item h4 {
		font-family: var(--font-primary);
		color: var(--secondary);
		margin-bottom: 0.3rem;
	}

	.contact-item p {
		font-family: var(--font-tertiary);
		color: var(--secondary);
		opacity: 0.7;
	}

	// Tablet
	@media (min-width: 768px) {
		.hero-title {
			font-size: 3rem;
		}

		.hero-subtitle {
			font-size: 1.4rem;
		}

		.hero-actions {
			flex-direction: row;
			justify-content: center;
		}

		.services-grid {
			grid-template-columns: repeat(2, 1fr);
		}

		.gallery-grid {
			grid-template-columns: repeat(3, 1fr);
		}

		.testimonials-grid {
			grid-template-columns: repeat(2, 1fr);
		}

		.contact-info {
			grid-template-columns: repeat(2, 1fr);
		}
	}

	// Desktop
	@media (min-width: 969px) {
		.hero {
			flex-direction: row;
			padding: 4rem 2rem;
		}

		.hero-content {
			text-align: left;
		}

		.hero-title {
			font-size: 3.5rem;
		}

		.hero-actions {
			justify-content: flex-start;
		}

		.about {
			flex-direction: row;
			justify-content: center;
		}

		.services-grid {
			grid-template-columns: repeat(4, 1fr);
		}

		.testimonials-grid {
			grid-template-columns: repeat(3, 1fr);
		}

		.stat-label {
			font-size: 0.85rem;
		}
	}
</style>