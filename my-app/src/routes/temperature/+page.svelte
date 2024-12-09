<script>
    import { goto } from "$app/navigation";

    let title = "Temperature Changes";
    let image1Big = false
    let image2Big = false

    //Home button function
    function goHome() {
        goto('/')
    }

    //Increase size of images
    function image1Size() {
        image1Big = !image1Big
    }
    function image2Size() {
        image2Big = !image2Big
    }
  </script>

<div class="header"> 
	<button class="header-title" on:click={goHome}>Climate Change</button> 
	</div>

  <div class="container">
    <h1>{title}</h1>
    <div class="section">
      <h2>Historical Temperature Data</h2>
      <p>
        Historical temperature data shows how the climate in your area has changed over the past decades. Understanding these trends is crucial for predicting future changes and preparing for their impacts.
      </p>
      <div class="image-container" on:click={image1Size}>
        {#if image1Big}
        <img src="/global-avg-temps.png" alt="Historic Average Temperatures" class="image-full" />
        {/if}
        {#if !image1Big}
        <img src="/global-avg-temps.png" alt="Historic Average Temperatures" class="image" />
        {/if}
      </div>
    </div>
    <div class="section">
      <h2>Projected Temperature Changes</h2>
      <p>
        Projections indicate how temperatures are expected to change in the coming years. These projections are based on various climate models and scenarios, helping to anticipate future conditions.
      </p>
      <div class="image-container" on:click={image2Size}>
        {#if image2Big}
        <img src="projected-temps.png" alt="Projected Temperatures" class="image-full" />
        {/if}
        {#if !image2Big}
        <img src="projected-temps.png" alt="Projected Temperatures" class="image" />
        {/if}
      </div>
    </div>
    <div class="section">
      <h2>Potential Impacts</h2>
      <p>
        Increased temperatures can have significant impacts on the environment, human health, and infrastructure. Understanding these impacts helps in planning and mitigation efforts to reduce adverse effects.
      </p>
    </div>
  </div>
  


<style>

    .header { 
	    background-color: #4CAF50; 
        color: white; 
	    padding: 1rem; 
	    display: flex; 
	    align-items: center; 
	}

    .header-title {
        align-self: center;
        font-size: 1.5rem;
        font-weight: 500;
        font-family: inherit;
        color: #fff;
        background: none;
        border: none;
        cursor: pointer;
        padding: 0;
        text-align: left;
    }
	
	.header-title:hover { 
	    background-color: #45a049; /* Button background color on hover */ 
	    color: white; /* Button text color on hover */ 
	} 

    .container {
        max-width: 800px;
        margin: 0 auto;
        padding: 2rem;
        font-family: Arial, sans-serif;
        color: #333;
    }
  
    h1 {
        color: #4CAF50;
        text-align: center;
    }
  
    .section {
        margin: 2rem 0;
    }
  
    .section h2 {
        color: #4CAF50;
    }
  
    .section p {
        color: #666;
        line-height: 1.6;
    }

    .image-container { 
        display: flex; 
        justify-content: center; 
        margin-top: 20px; 
    }

    .image { 
        max-width: 100%; 
        height: auto; 
        width: 320px;
        height: 190px;
    }

    .image-full { 
        max-height: 100%;
        max-width: 100%; 
    }

</style>