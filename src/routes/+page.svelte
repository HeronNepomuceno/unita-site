<script lang="ts">
	import { services, testimonials } from "../data";
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
				<a class="btn-primary" href="https://wa.me/5586998678703?text={encodeURIComponent("Olá, gostaria de agendar uma consulta!")}" target="_blank" >
						<svg viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg" class="whatsapp-icon">
							<path d="M17.472 14.382c-.297-.149-1.758-.867-2.03-.967-.273-.099-.471-.148-.67.15-.197.297-.767.966-.94 1.164-.173.199-.347.223-.644.075-.297-.15-1.255-.463-2.39-1.475-.883-.788-1.48-1.761-1.653-2.059-.173-.297-.018-.458.13-.606.134-.133.298-.347.446-.52.149-.174.198-.298.298-.497.099-.198.05-.371-.025-.52-.075-.149-.669-1.612-.916-2.207-.242-.579-.487-.5-.669-.51-.173-.008-.371-.01-.57-.01-.198 0-.52.074-.792.372-.272.297-1.04 1.016-1.04 2.479 0 1.462 1.065 2.875 1.213 3.074.149.198 2.096 3.2 5.077 4.487.709.306 1.262.489 1.694.625.712.227 1.36.195 1.871.118.571-.085 1.758-.719 2.006-1.413.248-.694.248-1.289.173-1.413-.074-.124-.272-.198-.57-.347m-5.421 7.403h-.004a9.87 9.87 0 01-5.031-1.378l-.361-.214-3.742.982.998-3.648-.235-.374a9.86 9.86 0 01-1.51-5.26c.001-5.45 4.436-9.884 9.888-9.884 2.64 0 5.122 1.03 6.988 2.898a9.825 9.825 0 012.893 6.994c-.003 5.45-4.437 9.884-9.885 9.884m8.413-18.297A11.815 11.815 0 0012.05 0C5.495 0 .16 5.335.157 11.892c0 2.096.547 4.142 1.588 5.945L.057 24l6.305-1.654a11.882 11.882 0 005.683 1.448h.005c6.554 0 11.890-5.335 11.893-11.893A11.821 11.821 0 0020.465 3.488"/>
						</svg>
					Agendar Consulta
				</a>
				<a 
					class="btn-instagram" 
					href="https://www.instagram.com/unita_teresina/" 
					target="_blank" 
					rel="noopener noreferrer"
				>
					Nos siga no Instagram
				</a>
			</div>
		</div>
		<div class="hero-image">
			<img class="image-banner" src="/banner.webp" alt="Unitá" />
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
				Nossa missão é oferecer serviços de estética e bem-estar em um ambiente acolhedor, promovendo a consciência do autocuidado para quem busca saúde de  forma integrada.
			</p>
		</div>
		<div class="about-image">
			<img class="image-placeholder" src="/logo.webp" alt="Unitá" />
		</div>
	</section>

	<div class="stats-container">
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
			<div class="stat">
				<div class="stat-number">10+</div>
				<div class="stat-label">Anos de experiência</div>
			</div>
		</div>
	</div>

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
						<p>Avenida Senador Area Leão, 1736 sala 4 - Zona Leste</p>
					</div>
				</div>
				<div class="contact-item">
					<span class="contact-icon">📞</span>
					<div>
						<h4>Telefone</h4>
						<p>+55 (86) 99867-8703</p>
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
			<div class="map">
				<iframe title="Localização Unitá" src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3974.159276253622!2d-42.7830862!3d-5.0779198!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x78e3bcdb8a7a003%3A0x1490d09546b34907!2sUnit%C3%A1-%20Est%C3%A9tica%20e%20Sa%C3%BAde%20Integrativa!5e0!3m2!1spt-BR!2sbr!4v1759277040521!5m2!1spt-BR!2sbr" width="600" height="450" style="border:0;" allowfullscreen={true} loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
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
		padding: 1.5rem;
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

	.btn-primary {
		align-items: center;
		display: flex;
		justify-content: center;
		font-family: var(--font-tertiary);
		font-weight: 500;
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
		white-space: nowrap;

		svg {
			height: 24px;
			width: 24px;
			fill: var(--on-surface);
			margin-right: 8px;
		}

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 6px 20px rgba(0, 64, 60, 0.4);
		}
	}

	.btn-instagram {
		display: flex;
		align-items: center;
		justify-content: center;
		font-family: var(--font-tertiary);
		font-weight: 500;
		padding: 1rem 2rem;
		max-height: 56px;
		border-radius: 30px;
		text-decoration: none;
		color: #fff;
		width: 100%;
		max-width: 280px;
		text-align: center;
		gap: 0.5rem;
		box-shadow: 0 4px 15px rgba(225, 48, 108, 0.3);
		background: linear-gradient(270deg, #f58529, #dd2a7b, #8134af, #515bd4);
		background-size: 800% 800%;
		animation: gradientShift 8s ease infinite;
		white-space: nowrap;

		&:hover {
			transform: translateY(-2px);
			box-shadow: 0 6px 20px rgba(225, 48, 108, 0.5);
		}
	}

	@keyframes gradientShift {
		0% { background-position: 0% 50%; }
		50% { background-position: 100% 50%; }
		100% { background-position: 0% 50%; }
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
		object-fit: cover;
		height: 360px;
	}

	.image-banner {
		aspect-ratio: 1;
		background: linear-gradient(135deg, var(--primary), var(--tertiary));
		border-radius: 50%;
		display: flex;
		align-items: center;
		justify-content: center;
		font-size: 5rem;
		box-shadow: 0 10px 40px rgba(203, 146, 118, 0.3);
		object-fit: cover;
		height: 480px;
	} 

	// Section Shared Styles
	section {
		padding: 3rem 1.5rem;
		scroll-margin-top: 80px;
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

	.stat-number {
		font-family: var(--font-primary);
		font-size: 2rem;
		color: var(--primary);
		font-weight: bold;
	}

	.stat-label {
		font-family: var(--font-tertiary);
		font-size: 0.8rem;
		color: var(--secondary);
		opacity: 0.8;
		margin-top: 0.5rem;
	}

	.about-image {
		width: 100%;
		max-width: 400px;
	}

	// Stats Container
	.stats-container {
		background: rgba(255, 255, 255, 0.5);
		padding: 1.5rem 3rem 1.5rem;
		scroll-margin-top: 80px;
	}

	.about-stats {
		display: grid;
		grid-template-columns: repeat(2, 1fr);
		gap: 1.5rem;
		max-width: 1200px;
		margin: 0 auto;
	}

	.stat {
		text-align: center;
		padding: 1.5rem;
		background: white;
		border-radius: 15px;
		box-shadow: 0 5px 20px rgba(0, 0, 0, 0.05);
		transition: transform 0.3s ease;
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
		object-fit: cover;

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


	.map {
		display: flex;
		justify-content: center;
		margin-top: 32px;
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

		.about-stats {
			grid-template-columns: repeat(3, 1fr);
		}
	}

	// Desktop
	@media (min-width: 969px) {
		.hero {
			flex-direction: row;
			padding: 0 2rem;
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

		.about-stats {
			grid-template-columns: repeat(4, 1fr);
		}

	}
</style>
