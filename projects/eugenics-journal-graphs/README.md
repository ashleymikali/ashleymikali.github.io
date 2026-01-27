# Historical Analysis of the Annals of Eugenics

A data-driven investigation of publication patterns, authorship, and research topics in the *Annals of Eugenics* (1925-1954).

📊 **[View Full Analysis](https://ashleymikali.com/projects/eugenics-journal-graphs/aoe-graphs.html)**

## Project Overview

This project examines the *Annals of Eugenics*, a scientific journal published from 1925 to 1954 (later renamed *Annals of Human Genetics*). Through web scraping and quantitative analysis, this study explores what was published during a controversial period in the history of genetics, statistics, and eugenics.

### Research Questions

1. How did publication volume change over the journal's 29-year run?
2. Which researchers were the most prolific contributors?
3. What research topics dominated the journal?

### Historical Context

The *Annals of Eugenics* was founded by Karl Pearson in 1925 during the height of the eugenics movement. The journal continued through World War II and was renamed in 1954 as the scientific community distanced itself from eugenics. This analysis examines publication patterns during this complex historical period.

## Methodology

### Data Collection

**Web Scraping Implementation:**
- Scraped article metadata from the journal's online archive
- Collected titles, authors, dates, and volume/issue information
- Processed 29 years of publications (Volumes 1-18)

**Technologies:**
- Python (BeautifulSoup, requests)
- Systematic extraction across all volumes and issues

### Data Processing

**Challenges:**
- Inconsistent formatting across volumes
- Complex author name variations (titles, degrees, initials)
- Multiple date formats

**Solutions:**
- Custom regex patterns for ~30 different academic credentials
- Author name normalization to `FirstInitial_LASTNAME` format
- Temporal data standardization

### Analysis Techniques

- Time series analysis of publication trends
- Text mining and word frequency analysis
- Authorship pattern analysis
- Data visualization with matplotlib and seaborn

## Key Findings

**Publication Trends:**
- Consistent output across most years with notable fluctuations
- Possible correlation with historical events (WWII, post-war period)

**Research Topics:**
- Dominant terms: "inheritance," "genetics," "correlation," "blood"
- Strong statistical/quantitative focus
- Mix of biological and mathematical terminology

**Top Authors:**
- Ronald Fisher (most prolific contributor)
- Other prominent researchers: J.B.S. Haldane, Karl Pearson, Lionel Penrose
- Notable presence of women researchers (Mary Noel Karn, Sylvia Lawler, Sarah Holt)

## Technical Stack

- **Language:** Python 3.x
- **Data Collection:** BeautifulSoup, requests
- **Data Processing:** pandas, regex
- **Analysis:** collections, sklearn
- **Visualization:** matplotlib, seaborn, wordcloud
- **Documentation:** Quarto

## Repository Structure

```
eugenics-journal-graphs/
├── data/
│   └── articles.csv              # Scraped article metadata
├── article-gatherer.py           # Web scraping script
├── aoe-graphs.qmd                # Main analysis (Quarto)
├── aoe-graphs.html               # Rendered analysis
└── README.md                     # This file
```

## Running the Analysis

### Prerequisites

```bash
pip install pandas matplotlib seaborn wordcloud scikit-learn beautifulsoup4 requests tabulate
```

### Scrape the Data

```bash
python article-gatherer.py
```

This will generate `data/articles.csv` with article metadata.

### Run the Analysis

```bash
quarto render aoe-graphs.qmd
```

Or open the `.qmd` file in RStudio/VS Code with Quarto extension.

## What This Project Demonstrates

✅ **Web scraping** - Systematic data extraction from online archives  
✅ **Data cleaning** - Complex text processing and normalization  
✅ **Regex mastery** - Pattern matching for academic credentials  
✅ **Historical research** - Applying data science to historical questions  
✅ **Text analysis** - Word frequency and topic extraction  
✅ **Data visualization** - Clear communication of patterns and trends  
✅ **Reproducible research** - Well-documented analysis with Quarto  

## Limitations

**Data Collection:**
- Only metadata analyzed (titles, authors, dates), not full article content
- Some formatting inconsistencies may have affected scraping accuracy

**Analysis:**
- Word frequency from titles provides limited insight into actual research content
- No citation analysis or assessment of research impact
- Quantitative analysis alone cannot capture full historical context

**Historical Interpretation:**
- Presence of authors/topics doesn't indicate endorsement or criticism
- Complex social and political context not fully captured by data analysis

## Future Directions

- Full-text analysis of article content
- Network analysis of co-authorship patterns
- Comparison with contemporary genetics/statistics journals
- Integration with institutional records and biographical data
- Exploration of how research published here influenced policy

## Broader Research Context

This project is part of a larger investigation into the history of eugenics at The College of Idaho, in Idaho, and in academia generally. Understanding what was published in the *Annals of Eugenics* helps contextualize the scientific legitimacy eugenics once held and how the field evolved.

## Ethical Considerations

This analysis examines a journal with a troubling history. The eugenics movement caused immense harm through forced sterilizations, discriminatory immigration policies, and ultimately contributed to genocidal ideologies. While some research published in this journal advanced legitimate statistical and genetic methods, it was often framed within or used to support eugenic ideology.

This project treats the data with historical awareness and recognizes that even "objective" scientific research can be embedded in and serve harmful social movements.

## Connect

- Portfolio: [ashleymikali.com](https://ashleymikali.com)
- GitHub: [@ashleymikali](https://github.com/ashleymikali)
- Email: ashkalirussell@gmail.com

## License

This project is open source for educational and research purposes. The historical data analyzed is in the public domain.

## Acknowledgments

- The College of Idaho for supporting this research
- The journal archive providers for maintaining access to historical scientific literature
- The broader academic community working to understand and reckon with the history of eugenics