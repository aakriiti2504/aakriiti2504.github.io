# Belly Button Bio Diversity 

## Background: 

Rosa is a biological researcher in a prominent microbiology laboratory. Many bacterial species are not well studied and many more remain unknown to science. Rosa's role is to discover and document these bacterias. In particular, Rosa is interested in bacterial species that have the ability to synthesize proteins that taste like beef.
Her lab has partnered with "Improbable Beef", a food startup to research candidate species. Labs across the country have had success in synthesizing meat from algae, fungii and microorganisms found on plant roots. However, Improbable Beef is still searching for the ilusive bacteria that will provide the perfect taste. Rosa has a 
hypothesis that there is a microorganism found on the human body that can provide the next best taste. 

Here's what Rosa knows so far:

The human body is a source for thousands types of bacteria and different types of the body harbor different species. Bacteria found in the gut are not the same species that are found on a person's eyelashes for example. furthermore, 
between individuals, the bacterial species may vary even in the same location. Rosa hypothizes that the ideal bacterial species to make synthetic beef may be found in the belly button. To test her hypothesis, Rosa has sampled the navals of people across the
country  to identify bacterial species that colonize our belly buttons. Each person's identity is annonymous and have been assigned an id number. Now Rosa wants to build a dashboard that both our research participants and fellow researchers can access. 
Those who participated in the study will be able to visit the website and select their id numbers to see which bacterial species live in their navals and gather other information. 


![Capture](https://user-images.githubusercontent.com/23488019/150728148-f0fd42e1-2a28-450a-bf0d-99b6240a27bb.PNG)


## Purpose : 

Roza has a partially completed dashboard that she needs to finish. She has a completed panel for demographic information and now needs to visualize the bacterial data for each volunteer. Specifically, her volunteers should be able to identify the top 10 bacterial species in their belly buttons. That way, if Improbable Beef identifies a species as a candidate 
to manufacture synthetic beef, Roza's volunteers will be able to identify whether that species is found in their navel.

## What I am Creating : 
This new assignment consists of four technical analysis deliverables. You will submit the following:

- Deliverable 1: Create a Horizontal Bar Chart
- Deliverable 2: Create a Bubble Chart
- Deliverable 3: Create a Gauge Chart
- Deliverable 4: Customize the Dashboard


## Tools Used :

- VS Code: We will use a text editor to create and edit HTML and JavaScript files.
- Web browser: We will use a web browser, such as Chrome, to view, inspect, and debug your visualizations. We will use Chrome in our examples.
- Command-line interface: We will use the command-line interface to run a local server. If you're a Mac user, this means Terminal. If you're a Windows user, you'll be using Git Bash.
- GitHub: As we will deploy our final data visualization on GitHub Pages, we will need a GitHub account.


## Results :

The finished website is shown below. This page has several components, which will be described in greater detail below.


![webpage](https://user-images.githubusercontent.com/23488019/150730760-ba660e6b-c6bc-4d07-846e-c6605e4c5c62.PNG)

#### Note : 

Note that since our Javascript code for this project reads a JSON data file from the local filesystem, that generates  CORS(Cross-Origin Resource Sharing) errors when run from a local browser. As a result I had to use my own web server. We can either use the default Python http server  by using, 

python -m http.server

or, we can use the Live Server extension in the VS Code. Also note that the URL bar in our Chrome browser shown in below is accessing the web page on localhost at the port specified:

http://127.0.0.1:5500/static/js/index.html

### Deliverable 1 : Horizontal Bar Chart : 

For the first deliverable, the code is written to create the arrays when a sample is selected from the dropdown menu. 
Code is written to create the trace object in the buildCharts() function, and it contains the y values(otu_ids) in descending order and the x values(sample_values) in descending order. The hover text is the otu_labels in descending order. Code is written to create the layout array in the buildCharts() function that creates a title for the chart.When the dashboard is first opened in a browser, ID 940’s data is displayed in the dashboard, and the bar chart has the top 10 sample_values in descending order, the top 10 sample_values as values and the otu_ids as the labels.

![barchart](https://user-images.githubusercontent.com/23488019/150730157-a38157ad-ccd2-472b-b7f4-d22b05f17074.PNG)

### Deliverable 2 : Bubble Chart :

Using JavaScript, Plotly, and D3.js, a bubble chart is created that will display the following when an individual’s ID is selected from the dropdown menu webpage:

- The otu_ids as the x-axis values.
- The sample_values as the y-axis values.
- The sample_values as the marker size.
- The otu_ids as the marker colors.
- The otu_labels as the hover-text values.


![bubblechart](https://user-images.githubusercontent.com/23488019/150730306-d4e5a8a1-e599-4899-af3e-0ecc3085fec9.PNG)

Using the variables that were created in Deliverable 1, we then created the bubble chart. The code for the trace object, the layout, and Plotly.newPlot() function to create the bubble chart was written accordingly.

To create the trace object for the bubble chart, we will assign the otu_ids, sample_values, and otu_labels to the x, y, and text properties, respectively.
For the mode and marker properties, the mode is "markers" and the marker property is a dictionary that defines the size, color, and colorscale of the markers. To create the layout for the bubble chart, I added a title, a label for the x-axis, margins, and the hovermode property. The hovermode should show the text of the bubble on the chart when you hover near that bubble.

### Deliverable 3 : Gauge Chart:

Using JavaScript, Plotly, and D3.js, a gauge chart was created that displays the weekly washing frequency's value, and displays the value as a measure from 0-10 on the progress bar in the gauge chart when an individual ID is selected from the dropdown menu.

![gauge chart](https://user-images.githubusercontent.com/23488019/150730490-ebbebdfb-8b58-4592-9975-a80598b912a9.PNG)

### Deliverable 4 : Customize the Dashboard : 

Use knowledge of HTML and Bootstrap, I chose the following upgrades to customize the webpage for the dashboard :

- 1. Add an image to the jumbotron - I used the following image in the bav=ckground of the jumbotron.

![customization 1](https://user-images.githubusercontent.com/23488019/150732175-aff94870-a052-442b-8d14-db41d2529487.PNG)


- 2. Add information about what each graph visualizes, either under or next to each graph - I added a brief description under each graph for better understanding of the graphs created.

- 3. Add background color or a variety of compatible colors to the webpage - I changed the background color and the color of the text under each chart.

![customized dashboard](https://user-images.githubusercontent.com/23488019/150735139-69246e07-898b-45d6-9cfb-d52014960e75.PNG)

This is how our customized dashboard looks like in the image shown above. 


