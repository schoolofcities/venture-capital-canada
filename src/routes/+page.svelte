<script>

	import TopSofC from "../lib/TopSofC.svelte";
	import "../assets/global-styles.css";
	import topVideo from "../assets/videoTest2.mp4";

</script>



<svelte:head>
	
	<meta
		name="viewport"
		content="width=device-width, initial-scale=1, minimum-scale=1"
	/>

</svelte:head>



<TopSofC/>

<main>

	<div class='intro'>
		<video src={topVideo}  muted preload autoplay loop playsinline></video> 
		<!-- poster='img.png' -->
		<div class='intro-overlay'>
			<h1>Canada’s High-Tech Startup Cities</h1>
		</div>
	</div>
	
	<div class="text">
		<div class="title">
			<!-- <h1>How reducing air pollution could extend thousands of lives</h1> -->
			<p><b><u>Research</u></b> Names<br>			<br>
			<b><u>Maps & Graphics</u></b>: Jeff Allen</p>
			<p>Funded by ....</p>
		</div>
		<p>
			Venture capital is the financial fuel that powers innovation and economic growth. This unique form of equity financing — which exchanges capital for shares in the enterprises they provide — has fueled the rise of revolutionary companies like Intel in semiconductors, Apple in personal computing, Genentech in biotech, Google in search, Twitter/X in social media, Chat GPT in artificial intelligence, and many more. 
		</p>
		<p>
			This report examines trends in the geography of venture capital across Canada for the decade spanning the 2010s and 2020s. Our data on venture capital comes from <a href="https://pitchbook.com/" target="_blank">PitchBook</a>, a leading research firm that tracks venture capital investment. We group the data in multi-year periods, 2009-11 and 2019-21, to limit annual fluctuations that can occur because of outsized investments in individual firms and/or metros in any given year.
		</p>
	</div>


</main>

<style>

	
</style>

