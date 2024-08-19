<script>

	import TopSofC from "../lib/TopSofC.svelte";

	import PerCapitaBar from "../lib/PerCapitaBar.svelte";

	import cartoInvestmentCanada from "../assets/carto-investment-canada.svg";
	import cartoInvestmentStates from "../assets/carto-investment-us.svg";
	import cartoDealsCanada from "../assets/carto-deals-canada.svg";
	import barChange from "../assets/bar-change.svg";

	import "../assets/global-styles.css";

</script>



<svelte:head>
	
	<meta
		name="viewport"
		content="width=device-width, initial-scale=1, minimum-scale=1"
	/>

</svelte:head>



<TopSofC/>

<main>

	<!-- <div class='intro'>
		<video src={topVideo}  muted preload autoplay loop playsinline></video> 
		<div class='intro-overlay'>
			
		</div>
	</div> -->

	<br>
	<br>
	<br>
	<br>

	
	<div class="text">
		<div class="title">
			<h1>Canada’s High-Tech Startup Cities</h1>
			<h3>The geography of venture capital investment across metro areas</h3>
			
			<!-- <h1>How reducing air pollution could extend thousands of lives</h1> -->
			<p>Research:  <a href="">Richard Florida</a> & <a href="">Karen King</a><br>
			Maps & Graphics: <a href="">Jeff Allen</a></p>
		</div>
		<p>
			<br>
			<span id="drop-cap">V</span>enture capital is the financial fuel that powers innovation and economic growth. This unique form of equity financing — which exchanges capital for shares in the enterprises they provide — has fueled the rise of revolutionary companies like Intel in semiconductors, Apple in personal computing, Genentech in biotech, Google in search, Twitter/X in social media, Chat GPT in artificial intelligence, and many more. 
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
		 <h2>The geography of venture capital <u>investment</u></h2>

		 <p>
			The figure below shows that have at least $100 million in VC investment from 2019 through 2021. These fourteen metros account for more than 90 percent of venture capital investment in Canada.
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

	<div class="img1000px" id="SF">
		<img src={cartoInvestmentStates} alt="SVG Image" />
	</div>

	<div class="text">
		<h2>
			The geography of venture capital <u>deals</u>
		</h2>
		<p>
			We now turn to the geography of venture capital deals. This measure is essentially a count of individual venture capital investments in high tech startups. It is useful because our previous measure of the level of venture capital investment can be biased toward larger, more established high-tech startup hubs, where startups tend to attract much higher levels of investment. 
		</p>
	</div>

	<div class="img1000px">
		<img src={cartoDealsCanada} alt="SVG Image" />
	</div>

	<div class="text">
		<p>
			Venture capital deals are also concentrated, though not as much as investment. The top ten metros account for more than 80 percent of all venture capital deals. Toronto again leads with more than 30 percent, followed by Vancouver with 17 percent and Montreal with 11 percent. The top three Canadian metros account for nearly 60 percent of venture capital deals – which is considerably higher than for the top three U.S. metros, which account for less than 40 percent (37 percent).
		</p>
		<p>
			Again, Canada’s leading metros trail U.S. metros by a large margin. San Francisco had 7,271 deals, New York had 5,787 deals, and Los Angeles had 3,344 deals – while no Canadian city had more than 1,000.
			
			<!-- Toronto accounts for less than 30 percent of Los Angeles’ venture capital deals, 17 percent of New York, and 13 percent of San Francisco. Vancouver’s is less that 20 percent of Los Angeles, 10 percent of New York, and 8 percent of San Francisco. Montreal is a little bit more than 10 percent of Los Angeles, 6 percent of New York, and 5 percent of San Francisco. Venture capital deals for the three leading Canadian metros make up less than 12 percent (11.6 percent) that of their three leading U.S. counterparts. -->
		</p>
		<br>
		<br>

		<h2>
			The geography of <u>per capita investment</u>
		</h2>
		<p>
			We now turn to venture capital investment on a per capita basis. Both of our previous measures – investments and venture capital deals– reflect the size of metro areas: larger metros are likely to have higher levels of investment simply by virtue of their larger size. To control for this, we now look at venture capital investment on a per capita basis. The pattern is rather different.
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
			<img src={barChange} alt="SVG Image"/>
		</div>
		<p>
			The biggest winner is Vancouver, which has seen its share of venture capital investment nearly double from 12 percent to nearly 24 percent. Quebec is the only other metro that has seen a significant increase in share of venture capital investment, increasing by nearly three percentage points. 
		</p>
		<p>
			The biggest losers are Toronto and Montreal. Toronto has witnessed a nearly 5 percentage point decline in its share of venture capital investment, while 8 percentage points.  Montreal ranks dead last on this metric, and Toronto is next to last of all 33 Canadian metros. A study by Richard Florida and Ian Hathaway placed Toronto in the third tier of advanced global startup hubs and Vancouver and Montreal in the fourth tier of distinguished global startup bubs. If anything, Toronto and Montreal have seen their status diminish as Vancouver’s has risen.
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
			While Toronto leads in overall venture capital investment and venture capital deals, this is mainly due to its larger economic size. It ranks fourth in venture capital investment per capita behind Vancouver, Kitchener-Cambridge-Waterloo, and Fredericton. 
		</p>
		<p>
			Across Canada, Vancouver has been the biggest winner in venture capital investment over the past decade, while both Toronto and Montreal have seen the share of venture capital investment decline substantially.
		</p>
		<p>
			Venture capital investment in Canadian metros is but a fraction of their U.S. counterparts. Venture investment in Canada’s three leading metros comprises just five percent of America’s three leading metros. The trend is even more startling when we consider per capita venture investment. And not just for leading centers like San Francisco –per capita venture investment in the U.S. college town of Boulder is more than six times that of Vancouver and ten times that of Toronto.
		</p>
	</div>

	<br>
	<br>
	<div class="text" >
		<p class="notes">
			<a href="">Richard Florida</a> is University Professor at the University of Toronto’s Rotman School of Management and Distinguished Scholar in Residence at the School of Cities.  <br><br><a href="">Karen King</a> is a Senior Research Associate at the University of Toronto’s Rotman School of Management and School of Cities.
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
	height: 1100px;
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
		width: 1000px;
		height: 1000px;
		overflow: hidden;
	}

	.img1000px img {
		width: 1000px;
		height: 1000px;
		transform: rotate(45deg) translateY(-50%);
		transform-origin: center left;
		position: absolute;
		top: 0px;
		left: -250px;
	}
	#SF {
		display: none;
	}
}

@media screen and (max-width: 860px) {
	.img1000px {
		width: 340px;
		height: 1000px;
		overflow: hidden;
	}
	.img1000px img {
		width: 1000px;
		height: 340px;
		transform: rotate(90deg) translateY(-100%);
		transform-origin: center left;
		position: absolute;
		top: -150px;
		left: -150px;
	}
}
	
</style>

