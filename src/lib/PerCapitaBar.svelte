<script>

	import {scaleLinear} from 'd3-scale';

	let data = [
		{
			"City": "Vancouver",
			"percapita": 2032
		},
		{
			"City": "Kitchener-Cambridge-Waterloo",
			"percapita": 1603
		},
		{
			"City": "Fredericton",
			"percapita": 1239
		},
		{
			"City": "Toronto",
			"percapita": 1224
		},
		{
			"City": "Québec",
			"percapita": 939
		},
		{
			"City": "Ottawa-Gatineau",
			"percapita": 885
		},
		{
			"City": "Saskatoon",
			"percapita": 746
		},
		{
			"City": "Montreal",
			"percapita": 739
		},
		{
			"City": "Guelph",
			"percapita": 556
		},
		{
			"City": "Calgary",
			"percapita": 533
		}
	]

	let divWidth;
	$: width = divWidth;

	const height = 450;
	const marginTop = 55;
	const marginRight = 50;
	const marginBottom = 20;
	const marginLeft = 0;

	$: xScale = scaleLinear()
		.domain([0, 2100])
		.range([0, width - marginRight - marginLeft]);

</script>



<div id="barChart" bind:offsetWidth={divWidth}>

	<svg height={height} width={width} id="svgChart">

		<text 
				x="{marginLeft}" 
				y="{20}"
				id="labelTitle"
				text-anchor="start" 
			>Venture Capital Investment Per Person</text>

		{#each [5, 500,1000,1500,2000] as l}

			<line 
				x1="{xScale(l)}" 
				y1="{marginTop}" 
				x2="{xScale(l)}" 
				y2="{height - marginBottom}"
				stroke="white" 
				stroke-width="4" 
				stroke-opacity="0.12"
			/>
		
		{/each}

		{#each data as d, i}

			<rect 
				id="bar"
				x="{marginLeft}" 
				y="{i * 40 + 60}" 
				height="{8}" 
				width="{xScale(d.percapita)}"
			/>

			<text 
				x="{marginLeft}" 
				y="{i * 40 + 55}"
				id="labelBar"
				text-anchor="start" 
			>{d.City}</text>

			<text 
				x="{xScale(d.percapita) + marginLeft + 3}" 
				y="{i * 40 + 70}"
				id="labelBar"
				text-anchor="start" 
				
			>${d.percapita}</text>

		{/each}

	</svg>

</div>


<style>

	#bar {
		fill: #00e3c1;
	}

	#labelBar {
		fill: #ffffff;
		font-size: 14px;
		font-family: RobotoRegular;
	}

	#labelTitle {
		fill: #ffffff;
		font-size: 19px;
		font-family: RobotoBold;
	}


</style>


