<script>
	import imgGeminiGeneratedImage from "../assets/gemini-generated-image.png?url";
	import imgGeminiGeneratedImageMobile from "../assets/gemini-generated-image-mobile.png?url";
	import imgGitHub from "../assets/github.png?url";
	import imgLinkedIn from "../assets/linkedin.png?url";
	import imgSignature from "../assets/signature.png?url";
	import gridPath from "./background_pattern.ts";

	const dotStyle = `
		  background-image: radial-gradient(circle, rgba(131,130,130, 0.5) 1.5px, transparent 1.5px);
	background-size: 6px 4px;
	background-repeat: repeat-x;
	background-position: 0 100%;
	padding-bottom: 1px;
	`;
</script>

<div class="root">
	<!-- Background Grid -->
	<div class="bg-grid" aria-hidden="true">
		<svg fill="none" preserveAspectRatio="none" viewBox="0 0 1944 1418.75">
			<path
				d={gridPath.p2525ab80}
				stroke="#C5C5C5"
				stroke-dasharray="10 10"
				stroke-opacity="0.2"
			></path>
		</svg>
	</div>

	<!-- Arcade image (right side, vertically flipped) -->
	<div class="arcade-img" aria-hidden="true">
		<img
			src={imgGeminiGeneratedImage}
			alt=""
			class="arcade-img-el arcade-img-el--desktop"
			style="mix-blend-mode: darken; opacity: 1;"
		/>
		<!-- <img
			src={imgGeminiGeneratedImageMobile}
			alt=""
			class="arcade-img-el arcade-img-el--mobile"
			style="mix-blend-mode: darken; opacity: 1;"
		/> -->
	</div>

	<!-- Content -->
	<div class="content">
		<!-- Nav -->
		<nav class="nav">
			<span class="nav-item">[h] home</span>
			<span class="nav-item">[p] projects</span>
			<span>[r] resume</span>
		</nav>

		<!-- Name -->
		<h1 class="name">Tejas Agarwal</h1>

		<!-- Bio -->
		<div class="bio">
			<p class="mb-0">
				I am a CS &amp; Human Sciences student at
				<a href="https://iiit.ac.in" target="_blank"> <span style={dotStyle}>IIIT-Hyderabad</span> </a>
				interested in Reinforcement Learning, Applied ML, Algorithmic Game Theory, Graph
				algorithms and how systems, computational or human, make decisions under uncertainty. 
			</p>
			<p class="mt-paragraph">
				Besides this, I enjoy discussing governance, financial markets, and
				behavioral sciences. I'm also learning 中文.
			</p>
			<p class="mt-paragraph mb-1">Currently:</p>
			<ul class="bio-list">
				<li>Developer @ <a href="https://saral.democratiseresearch.in/" target="_blank"> <span style={dotStyle}>Saral AI</span></a></li>
				<li>
					Undergraduate Researcher @ <a href="https://precog.iiit.ac.in" target="_blank"><span style={dotStyle}>Precog</span></a>
					under Prof. Ponnurangam Kumaraguru
				</li>
			</ul>
			<p class="mt-paragraph">
				In the past: graduated as Head Boy from
				<a href="https://dpsrkp.net" target="_blank"><span style={dotStyle}>DPS R. K. Puram;</span></a>
				Chief Director at
				<a href="https://exunclan.com" target="_blank"><span style={dotStyle}>Exun Clan;</span></a>
				and Program Manager (India and Asia Pacific) at
				<a href="https://codeday.org" target="_blank"><span style={dotStyle}>CodeDay</span>.</a>
			</p>
			<p class="mt-last">
				Some other random things I find interesting [<span style={dotStyle}
					>here</span
				>].
			</p>
		</div>

		<!-- Social Icons -->
		<div class="socials">
			<a href="https://github.com" target="_blank" rel="noopener noreferrer">
				<img
					src={imgGitHub}
					alt="GitHub"
					class="social-icon"
					style="mix-blend-mode: darken; opacity: 1;"
				/>
			</a>
			<a href="https://linkedin.com" target="_blank" rel="noopener noreferrer">
				<img
					src={imgLinkedIn}
					alt="LinkedIn"
					class="social-icon social-icon--linkedin"
					style="opacity: 1;"
				/>
			</a>
		</div>

		<!-- Signature -->
		<!-- <div class="signature">
			<img src={imgSignature} alt="Signature" style="mix-blend-mode: hard-light;" />
		</div> -->
	</div>
</div>

<style>
	/* ── Root ── */
	.root {
		position: relative;
		min-height: 100vh;
		width: 100%;
		overflow-x: hidden;
		background-color: #fffafa;
	}

	/* ── Background Grid ── */
	.bg-grid {
		position: absolute;
		inset: 0;
		overflow: hidden;
		pointer-events: none;
	}
	.bg-grid svg {
		position: absolute;
		display: block;
		width: 1944px;
		height: 1418px;
		/* Mobile offset */
		left: -335px;
		top: -24px;
	}
	@media (min-width: 768px) {
		.bg-grid svg {
			left: -88px;
			top: -79px;
		}
	}

	/* ── Arcade Image ── */
	.arcade-img {
		position: absolute;
		right: 0;
		bottom: 0;
		pointer-events: none;
		user-select: none;
	}
	.arcade-img-el {
		display: none;
		object-fit: contain;
	}
	/* Mobile image */
	.arcade-img-el--mobile {
		display: block;
		position: absolute;
		right: 0;
		bottom: 0;
		width: 160px;
		height: 200px;
		object-position: bottom right;
	}
	/* Desktop image */
	.arcade-img-el--desktop {
		display: none;
	}
	@media (min-width: 768px) {
		.arcade-img {
			width: 40%;
			height: 100%;
			min-height: 700px;
		}
		.arcade-img-el--mobile {
			display: none;
		}
		.arcade-img-el--desktop {
			display: block;
			position: absolute;
			left: 0;
			bottom: 0;
			width: 100%;
			height: 100%;
			object-position: bottom right;
		}
	}

	/* ── Content ── */
	.content {
		position: relative;
		z-index: 10;
		padding: 68px 47px 64px;
	}
	@media (min-width: 768px) {
		.content {
			padding: 55px 7.7% 80px;
			max-width: 1400px;
		}
	}

	/* ── Nav ── */
	.nav {
		font-family: "Space Mono", monospace;
		font-size: 13px;
		color: #272727;
		margin-bottom: 74px;
	}
	.nav-item {
		margin-right: 32px;
	}
	@media (min-width: 768px) {
		.nav {
			font-size: 15px;
			margin-bottom: 100px;
		}
		.nav-item {
			margin-right: 40px;
		}
	}

	/* ── Name ── */
	.name {
		margin-bottom: 24px;
		font-family: "Jersey 15", sans-serif;
		font-size: clamp(48px, 14vw, 68.895px);
		line-height: normal;
		color: #000000;
		font-style: normal;
		font-weight: normal;
	}
	@media (min-width: 768px) {
		.name {
			font-size: 50px;
		}
	}

	/* ── Bio ── */
	.bio {
		font-family: "Space Grotesk", "Noto Sans JP", sans-serif;
		font-weight: 400;
		font-size: 18px;
		color: #272727;
		line-height: 1.6;
	}
	@media (min-width: 768px) {
		.bio {
			max-width: calc(0.53 * 100vw);
		}
	}

	.bio-list {
		margin-top: 0 !important;
		list-style: disc;
		/* margin-left: 12px; */
		margin-bottom: 0;
	}
	.bio-list li + li {
		margin-top: 4px;
	}

	/* ── Socials ── */
	.socials {
		display: flex;
		align-items: center;
		gap: 16px;
		margin-top: 40px;
		position: relative;
		z-index: 10;
	}
	.social-icon {
		width: 38px;
		height: 37px;
		object-fit: contain;
	}
	.social-icon--linkedin {
		width: 39px;
	}

	/* ── Signature ── */
	.signature {
		margin-top: 12px;
		transform: rotate(2.26deg);
		width: 208px;
		height: 117px;
		margin-left: -14px;
		position: relative;
		z-index: 10;
	}
	.signature img {
		width: 100%;
		height: 100%;
		object-fit: cover;
	}

	/* ── Spacing utilities ── */
	.mb-0 {
		margin-bottom: 0;
	}
	.mb-1 {
		margin-bottom: 4px;
	}
	.mt-paragraph {
		margin-top: 16px;
	}
	.mt-last {
		margin-top: 28px;
	}
	@media (min-width: 768px) {
		.mt-paragraph {
			margin-top: 20px;
		}
		.mt-last {
			margin-top: 32px;
		}
	}

  a {
    all: unset; 
    cursor: pointer;
  }
</style>
