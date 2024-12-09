<script>
    import { page } from '$app/stores'
    import {  slide } from 'svelte/transition' 

    let showTemp = true
    let showPrecip = true
    let showSeaLvl = true
	let title = "Local Climate Impact Report";

    function toggleTemperature() {
        showTemp = !showTemp;
    }

    function togglePrecipitation() {
        showPrecip = !showPrecip;
    }

    function toggleSeaLevel() {
        showSeaLvl = !showSeaLvl;
    }
  </script>


<div class="header"> 
    {#if $page.url.pathname !== '/'}
	<a class="header-button" href="/">Home</a> 
    {/if}
	<div class="spacer"></div> <!-- Add any other elements or buttons here --> </div>
  <div class="container">
	<h1>Effects of Climate Change</h1>
	<div class="report-section">
        <h2 class="clickable" on:click={toggleTemperature}>Temperature Changes</h2>
        {#if showTemp}
	    <p in:slide out:slide>Rising temperatures are the most obvious effect of global warming.   <br><br>
	    <a class="button" href="/temperature">Learn More</a>
        </p>
        {/if}
	</div>
	<div class="report-section">
        <h2 class="clickable" on:click={togglePrecipitation}>Precipitation Patterns</h2>
        {#if showPrecip}
        <p in:slide out:slide>Changes in precipitation also implies major changes in the global ecosystem. See what it could mean for you. <br><br>
        <a class="button" href="/precipitation">Learn More</a>
        </p>
        {/if}
	</div>
	<div class="report-section">
        <h2 class="clickable" on:click={toggleSeaLevel}>Sea Level Rise</h2>
        {#if showSeaLvl}
        <p in:slide out:slide>Global Warming is causing the sea level to rise.  This is having major effects on coastal areas accross the globe. <br><br>
        <a class="button" href="/sea-level">Learn More</a>
        </p>
        {/if}
	</div>
  </div>
  

  
  <style>
	.container {
	  max-width: 800px;
	  margin: 0 auto;
	  padding: 2rem;
	  text-align: center;
	  font-family: Arial, sans-serif;
	  vertical-align: middle;
	}
  
	h1 {
	  color: #4CAF50;
	}
  
	.report-section {
	  margin: 2rem 0;
	}
  
	.report-section h2 {
	  color: #333;
	}
  
	.report-section p {
	  color: #666;
	}
  
	.button {
	  background-color: #4CAF50;
	  color: white;
	  padding: 10px 20px;
	  border: none;
	  cursor: pointer;
	  border-radius: 5px;
	  text-decoration: none;
	}
  
	.button:hover {
	  background-color: #45a049;
	}

	.header { 
	  background-color: #4CAF50; /* Background color for the header */ 
	  color: white; /* Text color */ 
	  padding: 1rem; /* Padding around the header */ 
	  display: flex; /* Use flexbox for alignment */ 
	  align-items: center; /* Vertically center items */ 
      height: 28px;
	}

	.header-button { 
	  background-color: white; /* Button background color */ 
	  color: #4CAF50; /* Button text color */ 
	  padding: 10px 20px; /* Button padding */ 
	  border: none; /* Remove default border */ 
	  cursor: pointer; /* Cursor changes to pointer on hover */ 
	  border-radius: 5px; /* Rounded corners */ 
	  text-decoration: none; /* Remove default text decoration */ 
	} 
	
	.header-button:hover { 
	  background-color: #45a049; /* Button background color on hover */ 
	  color: white; /* Button text color on hover */ 
	} 
	
	.spacer { 
	  flex: 1; /* Take up the remaining space */ 
	}

  h2 {
    color: #4CAF50;
  }

  .clickable {
    color: #4CAF50;
    cursor: pointer;
    text-decoration: underline;
    transition: color 0.3s ease, text-shadow 0.3s ease;
  }

  .clickable:hover {
    color: #45a049;
    text-shadow: 0 0 5px #45a049;
  }

  </style>