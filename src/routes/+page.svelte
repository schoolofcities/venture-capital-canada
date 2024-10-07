<script>

	import TopSofC from "../lib/TopSofC.svelte";

	import PerCapitaBar from "../lib/PerCapitaBar.svelte";

	import bubbleChange from "../assets/bubble-change.svg?raw";
	import cartoInvestmentCanada from "../assets/carto-investment-canada.svg?raw";
	import cartoInvestmentCanadaMobile from "../assets/carto-investment-canada-mobile.svg?raw";
	import cartoInvestmentStates from "../assets/carto-investment-us.svg?raw";
	import cartoDealsCanada from "../assets/carto-deals-canada.svg?raw";
	import cartoDealsCanadaMobile from "../assets/carto-deals-canada-mobile.svg?raw";
	import barChange from "../assets/bar-change.svg?raw";

	import "../assets/global-styles.css";

	let width = 1200;

</script>



<svelte:head>
	
	<meta
		name="viewport"
		content="width=device-width, initial-scale=1, minimum-scale=1"
	/>

</svelte:head>



<TopSofC/>

<main bind:offsetWidth={width}>

	<div class="top-image">
		<img src="./top.png"/>
	</div>

	<div class="text">

		<div class="title">
			<h1>Canada’s High-Tech Startup Cities</h1>
			<h3>The geography of venture capital investment across metro areas</h3>

			<p>Research: <a href="https://www.rotman.utoronto.ca/the-rotman-experience/our-community/people/florida-richard/" target="_blank">Richard Florida</a> & <a href="https://discover.research.utoronto.ca/22831" target="_blank">Karen King</a><br>
			Maps & Graphics: <a href="https://jamaps.github.io/" target="_blank">Jeff Allen</a></p>
		</div>
		<p>
			<br>
			<span id="drop-cap">V</span>enture capital is the financial fuel that powers innovation and economic growth. This unique form of equity financing — which exchanges capital for shares in the enterprises they provide — has fueled the rise of revolutionary companies like Intel in semiconductors, Apple in personal computing, Genentech in biotech, Google in search, Twitter/X in social media, ChatGPT in artificial intelligence, and many more. 
		</p>
		<p>
			Venture capital in Canada exploded from C$3.1 billion in the three year period of 2009-2011, to $23.5 billion in 2019-2021 — a nearly eightfold increase. But the benefits accrued to just a handful of cities who benefited from mega deals.
		</p>
		<div class="img350px">
			{@html bubbleChange}
		</div>
		<p>
			This study examines recent trends in the geography of venture capital across Canada. Our data on venture capital comes from <a href="https://pitchbook.com/" target="_blank">PitchBook</a>, a leading research firm that tracks venture capital investment. We group the data in multi-year periods, 2009-11 and 2019-21, to limit annual fluctuations that can occur because of outsized investments in individual firms and/or metros in any given year.
		</p>
		<p>
			Venture capital investment provides a measure of commercially relevant innovation. It offers a more direct gauge of such innovation than patents, which are commonly used by economists and economic geographers to measure innovation. Patents cover both basic scientific discoveries as well as commercial inventions. Many important commercial innovations are never patented, and many commercial patents are used for defensive purposes, to block competitors from gaining access to such innovations. As a measure of actual investment in high-growth startups, venture capital captures innovations with the potential to impact markets and change industries. 
		</p>
		<p>
			Our analysis employs several metrics for venture capital. The volume of venture capital investment provides an overall measure of the market value of venture capital. We look at counts of venture capital deals to account for the fact that more established high-tech centres tend to generate more competitive startups and attract larger venture investments. Because larger metro areas are likely to receive higher levels of venture capital simply as a result of their size, we also examine venture capital investment on a per capita basis. We also look at the change in venture capital investment over the decade-long period 2009-11 to 2019-2021. 
		</p>
		<br>
		<br>
		<!-- <Bubble/> -->
		 <h2>The geography of venture capital <u>investment</u></h2>

		 <p>
			The figure below shows metros that had at least $100 million in venture capital investment from 2019 through 2021. These fourteen metros account for more than 90 percent of venture capital investment in Canada.
		 </p>
		 <p>
			Toronto leads with roughly one third of venture capital investment, followed by Vancouver with slightly less than a quarter, and Montreal with roughly 14 percent.
		 </p>
		 
	</div>

	<div class="img1000px">

		{#if width > 1000}
			{@html cartoInvestmentCanada}
		{:else}
			{@html cartoInvestmentCanadaMobile}
		{/if}
		
	</div>

	<div class="text">
		<p>
			Venture capital investment in Canada is more concentrated than in the United States. The top three Canadian metros account for more than 70 percent (71.2 percent) of venture investment, compared to roughly 50 percent for the top three U.S. metros.
		</p>
		<p>
			That said, Canadian metros trail considerably behind the leading U.S. metros. Venture capital investment in Toronto is less than ten percent of that of New York and less than five percent of San Francisco. Venture investment in Vancouver is less than 3 percent of San Francisco’s, while Montreal’s is less than 2 percent of San Francisco’s. Venture capital investment in the three leading Canadian metros comprises just five percent (5.2 percent) of the venture capital investment in their three leading U.S. counterparts.
		</p>
	</div>

	{#if width > 1000}
		<div class="img1000px">
			{@html cartoInvestmentStates}
		</div>
	{/if}

	<div class="text">
		<h2>
			The geography of venture capital <u>deals</u>
		</h2>
		<p>
			We now turn to the geography of venture capital deals, i.e., individual venture capital investments in high tech startups. 
		</p>
	</div>

	<!-- <div class="img1000px">
		<img src={cartoDealsCanada} alt="SVG Image" />
	</div> -->

	<div class="img1000px">

		{#if width > 1000}
			{@html cartoDealsCanada}
		{:else}
			{@html cartoDealsCanadaMobile}
		{/if}
		
	</div>

	<div class="text">
		<p>
			Venture capital deals are also concentrated, though not as much as investment. The top ten metros account for more than 80 percent of all venture capital deals. Toronto again leads with more than 30 percent, followed by Vancouver with 17 percent and Montreal with 11 percent. The top three Canadian metros account for nearly 60 percent of venture capital deals – which is considerably higher than for the top three U.S. metros, which account for less than 40 percent (37 percent).
		</p>
		<p>
			Again, Canada’s leading metros trail U.S. metros by a large margin. San Francisco had 7,271 deals, New York had 5,787 deals, and Los Angeles had 3,344 deals – while no Canadian city had more than 1,000.
		</p>
		<br>
		<br>

		<h2>
			The geography of <u>per capita investment</u>
		</h2>
		<p>
			We now turn to venture capital investment on a per capita basis. Both of our previous measures – investments and venture capital deals – reflect the size of metro areas: larger metros are likely to have higher levels of investment simply by virtue of their larger size. To control for this, we now look at venture capital investment on a per capita basis. The pattern is rather different.
		</p>

		<br>

		<PerCapitaBar/>

		<p>
			Vancouver tops the list with just over $2,000 in venture capital investment per capita, followed by Kitchener-Cambridge-Waterloo and Fredericton, then Toronto. Montreal, while third in overall investment, falls to eighth in this ranking. 
		</p>
		<p>
			These amounts are just a fraction of leading U.S. metros. Per capita venture capital investment is over $35k in San Francisco (18 times greater than that of Vancouver), $24k in San Jose, and $13k in Boulder.
		</p>
	</div>
	
	<div class="text">

		<br>
		<br>
		<h2>
			Geographic <u>shifts</u> in venture capital investment
		</h2>
		<p>
			But which metropolitan areas have gained venture capital investment and where has it declined? This chart tracks the change in venture capital investment across metros for the period 2009-11 to 2019-21. There are clear winners and losers. 
		</p>
		<br>
		<div class="img350px">
			{@html barChange}
		</div>
		<p>
			The biggest winner is Vancouver, which has seen its share of venture capital investment nearly double from 12 percent to nearly 24 percent. Quebec is the only other metro that has seen a significant increase in share of venture capital investment, increasing by nearly three percentage points. 
		</p>
		<p>
			The biggest losers are Toronto and Montreal. Toronto has witnessed a nearly 5 percentage point decline in its share of venture capital investment, while Montreal saw a loss of 8 percentage points.
		</p>
	</div>

	<div class="text">
		<br>
		<br>
		<h2>
			Key takeaways
		</h2>
		<p>
			Several key findings emerge from our analysis. 
		</p>
		<p>
			First and foremost, venture capital investment in Canada is extremely concentrated, even more so than in the United States. The top three Canadian metros account for more than 70 percent of venture investment and nearly 60 percent of venture capital deals compared to roughly 50 percent and less than 40 percent respectively for the top three in the United States.
		</p>
		<p>
			While Toronto leads in overall venture capital investment and venture capital deals, this is partly due to its larger economic size. It ranks fourth in venture capital investment per capita behind Vancouver, Kitchener-Cambridge-Waterloo, and Fredericton.
		</p>
		<p>
			Across Canada, comparing 2019-2021 to a decade earlier, Vancouver has been the biggest winner in venture capital, while both Toronto and Montreal have seen slight declines in their share.
		</p>
		<p>
			Venture capital investment in Canadian metros is but a fraction of their U.S. counterparts. Venture investment in Canada’s three leading metros comprises just five percent of that of America’s three leading metros. To become a global leader in tech, Canada will need to attract far more venture capital in the future.
		</p>
	</div>
	
	<br>
	<br>
	<div class="text" >
		<p class="notes">
			<a href="https://www.rotman.utoronto.ca/the-rotman-experience/our-community/people/florida-richard/" target="_blank">Richard Florida</a> is University Professor at the University of Toronto’s Rotman School of Management and Distinguished Scholar in Residence at the School of Cities.  
			<br><br>
			<a href="https://discover.research.utoronto.ca/22831" target="_blank">Karen King</a> is a Senior Research Associate at the University of Toronto’s Rotman School of Management and School of Cities.
		</p>
		<br>
		<br>
	</div>

	<!-- Map Canada N -->


</main>



<style>

.img350px {
	margin: 0 auto;
	position: relative;
	/* height: 1100px; */
	max-width: 350px;
}

.img1000px {
	margin: 0 auto;
	position: relative;
	max-width: 1000px;
}

.img1000px img {
	margin: 0 auto;
	width: 1000px;
	/* height: 320px; */
	transform-origin: center;
}


@media screen and (max-width: 1000px) {
	.img1000px {
		width: 340px;
		height: 1100px;
		overflow: hidden;
	}
	.img1000px img {
		width: 1100px;
		height: 340px;
		transform: rotate(90deg) translateY(-100%);
		transform-origin: center left;
		position: absolute;
		top: -150px;
		left: -150px;
	}
}
	
</style>

