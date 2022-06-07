<script lang="ts">
	import { inview } from 'svelte-inview';

	let isInView;
	const options = {
		rootMargin: '-50px',
		unobserveOnEnter: true
	};

	const handleChange = ({ detail }) => {
		isInView = detail.inView;
	};

	let videoId = 'rv3Yq-B8qp4';
</script>

<section use:inview={options} on:change={handleChange}>
	<div id="video" class:animate={inView}>
		<iframe
			width="100%"
			height="100%"
			src="https://www.youtube-nocookie.com/embed/{videoId}"
			title="youtube video"
			frameborder="0"
			allow="clipboard-write; encrypted-media; picture-in-picture"
			allowfullscreen
		/>
	</div>
	<main />
</section>

<style>
	section {
		display: flex;
		max-width: 1400px;
		width: 100%;
		height: 400px;
		border-radius: 20px;
		overflow: hidden;
		background-size: cover;
		background-repeat: no-repeat;
		background-position: 0% 60%;
	}
	#video {
		width: 50%;
	}
	main {
		position: relative;
		width: 50%;
		background-color: hsl(218, 50%, 7%, 90%);
	}
</style>
