    <script>
        import { goto } from "$app/navigation";

        let title = "Precipitation Patterns";

        let image1Big = false
        let image2Big = false

        function goHome() {
        goto('/')
    }

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
          <h2>Historical Precipitation Data</h2>
          <p>
            Historical precipitation data shows how the amount and distribution of rainfall have changed over time in your area. This information is vital for understanding long-term trends and preparing for future changes.
          </p>
          <div class="image-container" on:click={image1Size}>
            {#if image1Big}
                <img src="global-precip-data.png" alt="Historic Precipitation Data" class="image-full" />
            {/if}
            {#if !image1Big}
                <img src="global-precip-data.png" alt="Historic Precipitation Data" class="image" />
            {/if}
          </div>
        </div>
        <div class="section">
          <h2>Projected Precipitation Changes</h2>
          <p>
            Projections provide insight into how precipitation patterns are expected to change due to various climatic factors. These predictions help in planning and adapting to potential shifts in weather patterns.
          </p>
          <div class="image-container" on:click={image2Size}>
            {#if image2Big}
                <img src="projected-precip.png" alt="Projected Precipitation" class="image-full" />
            {/if}
            {#if !image2Big}
                <img src="projected-precip.png" alt="Projected Precipitation" class="image" />
            {/if}
          </div>
        </div>
        <div class="section">
          <h2>Possible Impacts</h2>
          <p>
            Changes in precipitation can lead to significant impacts, such as increased flooding or drought. Understanding these impacts allows for better preparedness and mitigation strategies to minimize adverse effects.
          </p>
          <!-- Add information about possible impacts here -->
        </div>
        <!-- <a class="back-button" href="/">Back to Home</a> -->
      </div>
      


<style>
    	.header { 
	  background-color: #4CAF50; /* Background color for the header */ 
	  color: white; /* Text color */ 
	  padding: 1rem; /* Padding around the header */ 
	  display: flex; /* Use flexbox for alignment */ 
	  align-items: center; /* Vertically center items */ 
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
    
    /* .back-button {
        background-color: #4CAF50;
        color: white;
        padding: 10px 20px;
        border: none;
        cursor: pointer;
        border-radius: 5px;
        text-decoration: none;
        display: inline-block;
        margin-top: 2rem;
    }
    
    .back-button:hover {
        background-color: #45a049;
    } */

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