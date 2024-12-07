<div class="header"> 
	<a class="header-button" href="/">Home</a> 
	<div class="spacer"></div> <!-- Add any other elements or buttons here --> </div>

    <script>
        let title = "Sea Level Rise";
      </script>

      <div class="container">
        <h1>{title}</h1>
        <div class="section">
          <h2>Historical Sea Level Data</h2>
          <p>
            Historical sea level data provides insights into how sea levels have changed over time. This information is crucial for understanding long-term trends and preparing for future changes.
          </p>
          <!-- Add your charts or data visualizations here -->
        </div>
        <div class="section">
          <h2>Projected Sea Level Changes</h2>
          <p>
            Projections indicate how sea levels are expected to change in the coming years. These projections are based on various climate models and scenarios, helping to anticipate future conditions.
          </p>
          <!-- Add your projections or forecast models here -->
        </div>
        <div class="section">
          <h2>Potential Impacts</h2>
          <p>
            Rising sea levels can have significant impacts on coastal areas, including increased flooding and erosion. Understanding these impacts helps in planning and mitigation efforts to reduce adverse effects.
          </p>
          <!-- Add information about potential impacts here -->
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
      
        .back-button {
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
        }
</style>