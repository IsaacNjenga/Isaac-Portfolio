<script lang="ts">
	let sent = $state(false);
	let message = $state('');
	let name = $state('');

	const projects = [
		{
			number: '01',
			name: 'EasyManager',
			type: 'Product / E-commerce',
			description:
				'EasyManager is a business management and inventory system designed to help small and medium-sized businesses efficiently manage products, inventory, sales, expenses, customers, and business reporting from a centralized platform.',
			stack: ['Svelte', 'MongoDB', 'NodeJS', 'TailwindCSS'],
			className: 'project-nourish'
		},
		{
			number: '02',
			name: 'Toto Kalezi Foundation',
			type: 'Charity / Donation Platform',
			description:
				'A dedicated platform for the Toto Kalezi Foundation, focusing on empowering street children and vulnerable communities through donations and support.',
			stack: ['React', 'AntDesign', 'TailwindCSS'],
			className: 'project-orbit'
		},
		{
			number: '03',
			name: 'EndoCare',
			type: 'Medical Appointment / Health Records App',
			description:
				'A user-friendly mobile application that simplifies the process of managing medical appointments, accessing health records, and communicating with healthcare providers. Utilizes AI for early detection of diabetic and endocrine-related illnesses through medical image analysis.',
			stack: ['ReactJS', 'NodeJS', 'Express'],
			className: 'project-hush'
		},
		{
			number: '04',
			name: 'EasyDeal Furniture',
			type: 'Furniture / E-commerce',
			description:
				'A clean and modern online presence for customers to browse available furniture items, learn more about each product, and connect with the business.',
			stack: ['Svelte', 'NodeJS', 'Express'],
			className: 'project-nourish'
		}
	];

	const skills = [
		{ label: 'Frontend', items: 'TypeScript · React · Svelte · Next.js · HTML/CSS' },
		{ label: 'Backend', items: 'Node.js · REST · GraphQL · Auth · PostgreSQL' },
		{ label: 'Deployment', items: 'Cloudflare · AWS · CI/CD · Docker · Git' }
	];

	function handleSubmit() {
		sent = true;
		const phoneNumber = '254740900061';
		const payload = `Hi, my name is ${name}. ${message}`;

		const whatsappUrl = `https://wa.me/${phoneNumber}?text=${encodeURIComponent(payload)}`;

		window.open(whatsappUrl, '_blank');
	}
</script>

<svelte:head>
	<title>Isaac Njenga — Full-stack developer</title>
	<meta
		name="description"
		content="The portfolio of Isaac Njenga, a full-stack developer building thoughtful digital products."
	/>
	<link rel="preconnect" href="https://fonts.googleapis.com" />
	<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin="anonymous" />
	<link
		href="https://fonts.googleapis.com/css2?family=DM+Mono:wght@400;500&family=Manrope:wght@400;500;600;700;800&display=swap"
		rel="stylesheet"
	/>
</svelte:head>

<div class="site-shell">
	<nav class="nav" aria-label="Main navigation">
		<a class="wordmark" href="#top" aria-label="Isaac Njenga home"><span>IN</span><i></i></a>
		<div class="nav-links">
			<a href="#work">Work</a>
			<a href="#about">About</a>
			<a href="#skills">Skills</a>
		</div>
		<a class="nav-cta" href="#contact">Let's talk <span>↗</span></a>
	</nav>

	<main id="top">
		<section class="hero section-pad" aria-labelledby="hero-title">
			<div class="hero-copy">
				<p class="eyebrow">
					<span class="status-dot"></span> Available for select projects · 2024—25
				</p>
				<h1 id="hero-title">I make<br /><em>things</em> work.</h1>
				<p class="hero-intro">
					Full-stack developer crafting expressive, useful digital products from first sketch to
					final deploy.
				</p>
				<a class="round-link" href="#work" aria-label="Scroll to selected work"
					><span>See my work</span><b>↓</b></a
				>
			</div>
			<div class="hero-art" aria-label="Abstract portrait illustration" role="img">
				<div class="sun"></div>
				<div class="art-caption">Based in Nairobi<br />Working worldwide</div>
				<div class="art-mark">Isaac N<br /><small>24</small></div>
			</div>
			<!-- <div class="hero-foot">
				<span>Scroll to explore</span>
				<span class="hero-line"></span>
				<span>↘</span>
			</div> -->
		</section>

		<section class="marquee" aria-label="Capabilities">
			<div>
				Design-minded code <span>✳</span> Product thinking <span>✳</span> Full-stack craft
				<span>✳</span>
				User-oriented experience <span>✳</span> Collaboration <span>✳</span>
			</div>
		</section>

		<section id="work" class="work section-pad" aria-labelledby="work-title">
			<div class="section-heading">
				<p class="eyebrow">01 / Selected work</p>
				<h2 id="work-title">A few things<br /><em>I've made.</em></h2>
				<p class="section-note">
					Small team, ambitious ideas, and the good kind of technical challenge.
				</p>
			</div>
			<div class="project-list">
				{#each projects as project (project)}
					<article class="project-card">
						<div class={`project-visual ${project.className}`}>
							<span class="project-number">{project.number}</span>
							<div class="visual-shape"></div>
							<strong>{project.name}</strong>
						</div>
						<div class="project-info">
							<div>
								<p class="project-type">{project.type}</p>
								<h3>{project.name}</h3>
							</div>
							<p class="project-description">{project.description}</p>
							<div class="project-meta">
								<div class="tags">
									{#each project.stack as item (item)}<span>{item}</span>{/each}
								</div>
								<a href="#contact" aria-label={`Discuss ${project.name}`}>Discuss the project ↗</a>
							</div>
						</div>
					</article>
				{/each}
			</div>
		</section>

		<section id="about" class="about section-pad" aria-labelledby="about-title">
			<div class="about-label">
				<p class="eyebrow">02 / About me</p>
				<span class="vertical-rule"></span><span>Curious by default</span>
			</div>
			<div class="about-copy">
				<h2 id="about-title">
					The space between<br /><span class="font-thin text-red-600 italic">idea & outcome.</span>
				</h2>
				<div class="about-columns">
					<p>
						I’m Isaac, a full-stack developer with a soft spot for the messy middle: turning a messy
						idea into something clear, fast, and genuinely pleasant to use.
					</p>
					<p>
						For the past 5 years I’ve worked across product, design, and engineering teams to build
						software that earns its place in the world. I care about the details, but I care even
						more about the people using them.
					</p>
				</div>
				<a
					class="text-link"
					href="mailto:njengaisaac789@gmail.com?subject=Project%20inquiry%20for%20Isaac%20Njenga"
					aria-label="Email Isaac Njenga about a project">Email me <span>↗</span></a
				>
			</div>
		</section>

		<section id="skills" class="skills section-pad" aria-labelledby="skills-title">
			<div class="section-heading skills-heading">
				<p class="eyebrow">03 / The toolkit</p>
				<h2 id="skills-title">Tools are just<br /><em>the beginning.</em></h2>
			</div>
			<div class="skill-list">
				{#each skills as skill, i (skill)}
					<div class="skill-row">
						<span>0{i + 1}</span>
						<h3>{skill.label}</h3>
						<p>{skill.items}</p>
						<b>↗</b>
					</div>
				{/each}
			</div>
		</section>

		<section id="contact" class="contact section-pad" aria-labelledby="contact-title">
			<div class="contact-top">
				<p class="eyebrow">04 / Start a conversation</p>
				<span>Have a project in mind?</span>
			</div>
			<h2 id="contact-title">Let's make<br /><em>something good.</em></h2>
			<div class="contact-bottom">
				<p>
					Tell me a little about what you’re building, where you are in the process, and what would
					make this a win.
				</p>
				<form onsubmit={handleSubmit}>
					{#if sent}
						<p class="success-message">Thanks — your note is on its way. <span>✳</span></p>
					{:else}
						<label
							><span>Your name</span><input
								type="text"
								bind:value={name}
								name="name"
								required
							/></label
						>
						<label
							><span>A few words</span><textarea
								placeholder="I have an idea..."
								rows="2"
								id="message"
								bind:value={message}
								required></textarea></label
						>
						<button type="submit">Send inquiry <span>↗</span></button>
					{/if}
				</form>
			</div>
		</section>
	</main>

	<footer class="footer">
		<a class="wordmark" href="#top"><span>IN</span><i></i></a>
		<p>© {new Date().getFullYear()} Isaac Njenga. Built with care.</p>
		<div class="socials">
			<a href="https://github.com/IsaacNjenga" target="_blank" rel="noreferrer">GitHub ↗</a><a
				href="https://www.linkedin.com/in/isaacnjenga"
				target="_blank"
				rel="noreferrer">LinkedIn ↗</a
			>
		</div>
	</footer>
</div>
