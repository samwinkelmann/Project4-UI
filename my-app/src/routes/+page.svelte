<script>
	let title = "Local Climate Impact Report";
  </script>

  
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
  </style>

<div class="header"> 
	<a class="header-button" href="/">Home</a> 
	<div class="spacer"></div> <!-- Add any other elements or buttons here --> </div>
  <div class="container">
	<h1>Effects of Climate Change</h1>
	<div class="report-section">
	  <h2>Temperature Changes</h2>
	  <p>Explore the historical and projected temperature changes in your area.</p>
	  <a class="button" href="/temperature">View Report</a>
	</div>
	<div class="report-section">
	  <h2>Precipitation Patterns</h2>
	  <p>Learn about changes in precipitation patterns and their effects on your community.</p>
	  <a class="button" href="/precipitation">View Report</a>
	</div>
	<div class="report-section">
	  <h2>Sea Level Rise</h2>
	  <p>Understand the implications of sea level rise and what it means for coastal areas.</p>
	  <a class="button" href="/sea-level">View Report</a>
	</div>
  </div>
  