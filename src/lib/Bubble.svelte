<script>
	import * as d3 from "d3";
	import { onMount } from 'svelte';
  
	// Example data
	let data = [
	  { "city": "Toronto", "total": 900 },
	  { "city": "New York", "total": 4231 },
	  { "city": "Los Angeles", "total": 7000 },
	  { "city": "Chicago", "total": 200 }
	];
  
  // Dimensions
  const width = 800;
  const height = 600;

  // Create a hierarchy from the data
  const root = d3.hierarchy({ children: data })
    .sum(d => d.total);

  // Create the pack layout
  const pack = d3.pack()
    .size([width, height])
    .padding(5);

  // Apply the pack layout to the hierarchy
  pack(root);
</script>

<svg width={width} height={height}>
  {#each root.leaves() as leaf}
    <circle
      cx={leaf.x}
      cy={leaf.y}
      r={leaf.r}
      fill="steelblue">
    </circle>
    <text
      x={leaf.x}
      y={leaf.y}
      text-anchor="middle"
      alignment-baseline="middle"
      fill="white"
      font-size="12px">
      {leaf.data.city}
    </text>
  {/each}
</svg>
