<script>
	import * as d3 from "d3";
	import { geoPath, geoOrthographic, geoConicEqualArea } from "d3-geo";
	import provincesData from './globe-data/provinces.geo.json'; // Import the JSON file directly
  
	let width = 900, height = 800;
	let projection, path;
	let provinces = [];
  
	// Set up the projection and path
	projection = geoConicEqualArea()
    .center([0, 64])  // Latitude center
    .rotate([101, 0])  // Longitude rotation to focus on Canada
    .parallels([49, 77])  // Define standard parallels
    .scale(1000)  // Adjust scale as needed
    .translate([width / 2, height / 2]);
  
	path = geoPath().projection(projection);
  
	// Directly assign the imported data to provinces
	provinces = provincesData.features;
  
	// Helper function to generate path for each province
	function getProvincePath(province) {
	  return path(province);
	}
  </script>
  
  <style>

	.globe {
	  fill: #01062f;
	  stroke: #151515;
	  stroke-width: 0.5px;
	}
  
	.province {
	  fill: #1E3765;
	  stroke: #01062f;
	  stroke-width: 1px;
	}
  </style>
  
  <svg {width} {height}>
	<!-- Draw the globe -->
	<path
	  class="globe"
	  d={path({ type: "Sphere" })}
	/>
  
	<!-- Draw the provinces using {#each} -->
	{#each provinces as province}
	  <path
		class="province"
		d={getProvincePath(province)}
	  />
	{/each}
  </svg>
