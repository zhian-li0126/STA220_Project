# STA220_Project
# Analyzing Global News Discourse on the Russo-Ukrainian War (2022–2025)

## Project Overview
This project analyzes global news coverage of the Russo-Ukrainian War from 2022-2025 through natural language processing of news headlines from three major international news networks: BBC, The Guardian, and The New York Times. The research provides insights into how major mainstream media outlets report on international political events through keyword analysis, topic modeling, and sentiment exploration.

## Authors
- **Zhian Li** - Department of Biological and Agricultural Engineering, University of California, Davis
  - Contributions: Web scraping, LDA topic modeling, sentiment analysis
  - Contact: zanli@ucdavis.edu
  
- **Haojian Li** - Department of Communication, University of California, Davis
  - Contributions: Web scraping, visualization, interactive visualization
  - Contact: hiji@ucdavis.edu

## Data Collection
The project collected news headlines related to the Russo-Ukrainian War from three major news outlets:
- BBC (8,388 headlines)
- The Guardian (27,749 headlines)
- The New York Times (7,201 headlines)

Total dataset: 43,338 headlines from 2022 to 2025

Data was collected using:
- BeautifulSoup for BBC data
- Documented APIs for The Guardian and The New York Times
- Automated scripts with relevant keywords (e.g., "Ukraine," "Russia," "conflict," "war")

All data is stored in a uniform JSON format:
```json
{
  "Article Title 1": [
    "MM-DD-YYYY",
    "Identified Keywords (if applicable)",
    "URL",
    "Source/Journal"
  ],
  "Article Title 2": [
    "MM-DD-YYYY",
    "Identified Keywords (if applicable)",
    "URL",
    "Source/Journal"
  ],
  ...
}
```

## Methods

### Preprocessing
- Text normalization (lowercase conversion)
- Name unification for political figures and countries
- Stopword removal and noise reduction
- Tokenization and part-of-speech tagging
- Named entity recognition (NER)

### Analysis Techniques
1. **Title Frequency Analysis**: Identified most common political actors, locations, and concepts
2. **Latent Dirichlet Allocation (LDA)**: Uncovered 5 major topics in the news coverage
3. **Sentiment Analysis**: Used TextBlob to calculate polarity scores for headlines
4. **Geospatial Analysis**: Created heat maps and visualizations of regions mentioned

### Visualization
- Matplotlib, Seaborn, and Plotly for data visualization
- Interactive world map (hosted on GitHub Pages) displaying country-level mention frequencies
- Heat maps focused on Ukraine's regional coverage

## Key Findings

### Topic Modeling
Five primary topics were identified:
1. War actors (Ukraine, Russia, Vladimir Putin)
2. Conflict events (invasion, military actions)
3. International diplomatic efforts (UK, EU, NATO)
4. Economic impacts (energy, prices, crisis)
5. Israel-Gaza situation (parallel conflict coverage)

### Sentiment Analysis
- 62.6% of headlines were neutral
- 22.2% were positive
- 15.2% were negative
- The Guardian showed highest average positive sentiment (0.027)
- October 2024 showed the only instance of negative average sentiment

### Geographic Focus
- Most mentioned countries: Ukraine, Russia, United States, United Kingdom, China, Israel
- Most mentioned leaders: Putin, Biden, Johnson, Zelensky
- Most referenced Ukrainian regions: Kyiv, Kherson, Zaporizhzhia, Donbas

## Code Structure
The project code is organized into several primary components:

```
/
├── main/            # Data preprocessing modules
│   ├── text_processing.py # Text normalization, tokenization
│   └── api_scrap.py  # Name standardization
│
├── visualization/         # Visualization
│
└── data/                  # Data storage
```

## Installation and Setup

### Requirements
- Python 3.8+
- NLTK
- scikit-learn
- TextBlob
- BeautifulSoup4
- Matplotlib
- Seaborn
- Plotly


## Interactive Visualization
The interactive visualization of country-level mentions is available at:
[https://username.github.io/russo-ukrainian-war-news-analysis/](https://username.github.io/russo-ukrainian-war-news-analysis/)

## References
1. Blei, D. M., Ng, A. Y., & Jordan, M. I. (2003). Latent dirichlet allocation. Journal of Machine Learning Research, 3(Jan), 993-1022.
2. Ran, T., & Liu, Z. (2024). "The russia-ukraine war" or "the us-russia war"? Thematic analysis of global times' coverage of the russia-ukraine war. Media Asia, 51(1), 3-32.

## License
[MIT License](LICENSE)
