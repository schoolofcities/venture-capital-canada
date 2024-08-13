<script>

	import TopSofC from "../lib/TopSofC.svelte";
	import Bubble from "../lib/Bubble.svelte";

	import cartoInvestmentCanada from "../assets/carto-investment-canada.svg";
	import cartoInvestmentStates from "../assets/carto-investment-us.svg";

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
			<p><b><u>Research</u></b> Richard Florida & Karen King<br>
			<b><u>Maps & Graphics</u></b>: Jeff Allen</p>
		</div>
		<p>
			<br>
			<span style="font-size:100px; padding-right:-40px;">V</span>enture capital is the financial fuel that powers innovation and economic growth. This unique form of equity financing — which exchanges capital for shares in the enterprises they provide — has fueled the rise of revolutionary companies like Intel in semiconductors, Apple in personal computing, Genentech in biotech, Google in search, Twitter/X in social media, Chat GPT in artificial intelligence, and many more. 
		</p>
		<p>
			This report examines trends in the geography of venture capital across Canada for the decade spanning the 2010s and 2020s. Our data on venture capital comes from <a href="https://pitchbook.com/" target="_blank">PitchBook</a>, a leading research firm that tracks venture capital investment. We group the data in multi-year periods, 2009-11 and 2019-21, to limit annual fluctuations that can occur because of outsized investments in individual firms and/or metros in any given year.
		</p>
		<p>
			Venture capital investment provides a measure of commercially relevant innovation. It offers a more direct gauge of such innovation than patents, which are commonly used by economists and economic geographers to measure innovation. Patents cover both basic scientific discoveries as well as commercial inventions. Many important commercial innovations are never patented, and many commercial patents are used for defensive purposes, to block competitors from gaining access to such innovations. As a measure of actual investment in high-growth startups, venture capital captures innovations with the potential to impact markets and change industries. 
		</p>
		<p>
			Our analysis employs several metrics for venture capital. The volume of venture capital investment provides an overall measure of the market value of venture capital. We look at counts of venture capital deals to account for the fact that more established high-tech centres tend to generate more competitive startups and attract larger venture investments. Because larger metro areas are likely to receive higher levels of venture capital simply as a result of their size, we examine venture capital investment on a per capita basis. We also look at the change in venture capital, investment over the decade-long period 2009-11 to 2019-2021 to identify metros which are gaining venture capital as opposed to those where it is declining. 
		</p>
		<br>
		<br>
		<!-- <Bubble/> -->
		 <h2>The geography of venture capital investment</h2>

		 <p>
			The figure below shows that have at least $100 million in VC investment from 2019 through 2021. These fourteens metros account for more than 90 percent of venture capital investment in Canada.
		 </p>
		 <p>
			Toronto leads with roughly one third of venture capital investment, followed by Vancouver with slightly less than a quarter, and Montreal with roughly 14 percent.
		 </p>
		 
	</div>

	<div class="img1000px">
		<img src={cartoInvestmentCanada} alt="SVG Image" />
	</div>

	<div class="text">
		<p>
			Venture capital investment in Canada is more concentrated than in the United States. The top three Canadian metros account for more than 70 percent (71.2 percent) of venture investment, compared to roughly 50 percent for the top three U.S. metros.
		</p>
		<p>
			That said, Canadian metros trail considerably behind the leading U.S. metros. Venture capital investment in Toronto is less than ten percent of that of New York and less than five percent of San Francisco. Venture investment in Vancouver is less than ten percent that of Boston, 6 percent of New York, and 3 percent of San Francisco. Montreal’s is less than 5 percent of Boston, 4 percent of New York, and 2 percent of San Francisco. Venture capital investment in the three leading Canadian metros comprises just five percent (5.2 percent) of the venture capital investment in their three leading U.S. counterparts.
		</p>
	</div>

	<div class="img1000px">
		<img src={cartoInvestmentStates} alt="SVG Image" />
	</div>

	<div class="text">
		<h2>
			The geography of venture capital deals
		</h2>
		<p>
			We now turn to the geography of venture capital deals (see Table 2). This measure is essentially a count of individual venture capital investments in high tech startups. It is useful because our previous measure of the level of venture capital investment can be biased toward larger, more established high-tech startup hubs, where startups tend to attract much higher levels of investment. 
		</p>
	</div>

	

	

	<!-- Map Canada $ -->

	<!-- Bubble Chart comparing to US $ -->



	<!-- Map Canada N -->

	<!-- Bubble Chart comparing to US N -->


	<!-- Per capita ranking -->


	<!-- Change over time ranking -->


</main>

<style>

	
</style>

