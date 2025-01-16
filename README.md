# Movie Network Analysis Project

## Project Overview

This project involves scraping and analyzing data from Rotten Tomatoes' "Movies on Netflix 2024 (At Home)" category. The primary goal is to construct and analyze a network graph representing relationships between movies based on their Tomatometer scores. The project employs network analysis techniques, including PageRank, clustering coefficients, and degree distribution, to uncover insights about movie relationships and importance.

## Data Collection

### Scraping Process

1. **Data Source**: Rotten Tomatoes' "Movies on Netflix 2024 (At Home)" category.
2. **Tool Used**: Apify Rotten Tomatoes Scraper ([link](https://apify.com/rado.ch/rotten-tomatoes-scraper)).
3. **Scraping Input**: URL - [Rotten Tomatoes Netflix Movies](https://www.rottentomatoes.com/browse/movies_at_home/affiliates\:netflix?page=5).
4. **Settings**: Maximum results set to 500.
5. **Output**: 864 results scraped in 8 hours.
6. **Data Export**: Extracted into CSV format.

### Collected Data Attributes

- Aspect Ratio
- Audience Score
- Box Office (Gross USA)
- Cast
- Director
- Distributor
- Genre
- Original Language
- Producer
- Production Company
- Rating
- Release Date (Streaming)
- Release Date (Theaters)
- Rerelease Date (Theaters)
- Runtime
- Sound Mix
- Synopsis
- Title
- Tomatometer
- URL
- Collection View
- Writer

### Cleaned Dataset

After cleaning, the following attributes were retained:

- Audience Score
- Box Office (Gross USA)
- Genre
- Original Language
- Release Date (Theaters)
- Runtime
- Title
- Tomatometer

## Network Graph Construction

- **Nodes**: Movie titles.
- **Edges**: Relationships based on Tomatometer scores.
  - **Weight**: Inversely proportional to the similarity in scores (higher score difference = higher edge weight).

The network graph consists of:

- **Nodes**: 264 movies.
- **Edges**: Numerous, weighted connections between movies.
- **Visualization**:
  - Graph size: 50x50 (default) or 250x250 (requires heavy computational resources).
  - A 25,000x25,000 PNG image of the network is included in the project zip file.

## Analysis Techniques

### 1. PageRank

- Assesses the significance of nodes (movies) based on their connectivity.
- Higher PageRank scores indicate more influential or well-connected movies.
- Example scores:
  - "Fallen Leaves": 0.00522
  - "Tótem": 0.00522
  - "Four Daughters": 0.00548

### 2. Degree Distribution

- Plots the distribution of connections (edges) per node.

### 3. Average Clustering Coefficient

- Measures the tendency of nodes to form tightly-knit groups.
- **Value**: 1.0, indicating a fully connected network.

## Results and Insights

- **Graph Visualization**: High-rated movies are placed lower, and low-rated movies are placed higher in the graph.
- **Clustering Coefficient**: Indicates a highly interconnected network.
- **PageRank**: Highlights central movies in the network.
- **Degree Distribution**: Reflects the diversity in movie connections.

### Insights

- The graph reveals relationships between movies based on ratings.
- It can help predict movie preferences or recommend movies based on similar scores.

### Further Questions

1. Can expanding the dataset provide deeper insights?
2. Can analysis methods improve network efficiency?

## Future Work

- Create genre-specific or director-specific graphs.
- Analyze relationships based on additional attributes like release year or production company.

## How to Use

1. Load the CSV data.
2. Run the provided scripts to generate the network graph and calculate metrics.
3. Visualize and analyze results.

## Tools and Technologies

- **Apify**: For web scraping.
- **NetworkX**: For graph construction and analysis.
- **Matplotlib**: For data visualization.

---

**Contact**: For queries or contributions, please contact [Dhruv Singh](mailto\:dsingh28@hawk.iit.edu).

---

Download the project assets, including the 25,000x25,000 PNG image and analysis scripts, in the provided zip file.