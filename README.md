# Smartphone Sentiment Analysis

A comprehensive sentiment analysis project that analyzes Reddit discussions about various smartphone brands and models to understand public sentiment and value perception.

## Project Overview

This project collects and analyzes Reddit posts and comments about smartphones to determine:
- Overall sentiment towards different smartphone brands
- Value-for-money perception across brands
- Public opinion trends in smartphone discussions

## Key Features

- **Reddit Data Collection**: Automated scraping of smartphone-related discussions from multiple subreddits
- **Sentiment Analysis**: Uses NLTK's VADER sentiment analyzer for accurate sentiment scoring
- **Brand Analysis**: Compares sentiment across major smartphone brands
- **Value Perception**: Special analysis of price and value-related discussions
- **Data Visualization**: Generates insightful charts and graphs

## Analyzed Brands

The project analyzes sentiment for the following smartphone brands and models:
- **Samsung**: Galaxy series, S24 models
- **Apple**: iPhone series, iPhone 15
- **OnePlus**: OnePlus 12
- **Nothing**: Phone (2)
- **Xiaomi/Redmi**: Redmi Note 13
- **Tecno**: Pova series
- **Infinix**: Note series
- **iQOO**: Neo series

## Technical Stack

- **Python**: Core programming language
- **PRAW**: Reddit API wrapper for data collection
- **Pandas**: Data manipulation and analysis
- **NLTK**: Natural language processing and sentiment analysis
- **Matplotlib & Seaborn**: Data visualization
- **Jupyter Notebook**: Interactive development environment

## Project Structure

```
sentiment/
├── Smartphone_Sentiment_Analysis.ipynb    # Main analysis notebook
├── smartphone_sentiment_analysis (1).csv  # Processed dataset (131MB)
├── README.md                              # This file
└── .gitignore/                           # Git ignore patterns
```

## Dataset Information

The processed dataset contains **512,904 rows** with the following columns:
- `Id`: Unique identifier for each post/comment
- `neg`, `neu`, `pos`: Negative, neutral, and positive sentiment scores
- `compound`: Overall sentiment score (-1 to 1)
- `source_subreddit`: Reddit subreddit where the content was found
- `text`: Original text content
- `brand`: Identified smartphone brand
- `created_utc`: Timestamp of the post/comment
- `is_about_value`: Boolean indicating if the content discusses value/price

## Getting Started

### Prerequisites

1. **Python 3.7+** installed on your system
2. **Reddit API credentials** (Client ID and Client Secret)

### Installation

1. Clone this repository:
```bash
git clone <repository-url>
cd sentiment
```

2. Install required packages:
```bash
pip install pandas praw matplotlib seaborn nltk tqdm python-dotenv
```

3. Set up environment variables:
Create a `.env` file in the project root with your Reddit API credentials:
```
REDDIT_CLIENT_ID=your_client_id_here
REDDIT_CLIENT_SECRET=your_client_secret_here
```

### Running the Analysis

1. Open the Jupyter notebook:
```bash
jupyter notebook Smartphone_Sentiment_Analysis.ipynb
```

2. Run all cells in the notebook to:
   - Collect data from Reddit
   - Perform sentiment analysis
   - Generate visualizations
   - Export results to CSV

## Output Files

The analysis generates several output files:
- `smartphone_sentiment_analysis.csv`: Complete dataset with sentiment scores
- `sentiment_by_brand.png`: Chart showing average sentiment by brand
- `sentiment_by_value.png`: Chart showing value-focused sentiment analysis

## Analysis Methodology

1. **Data Collection**: Scrapes posts and comments from relevant subreddits
2. **Text Processing**: Cleans and prepares text data for analysis
3. **Sentiment Scoring**: Uses VADER sentiment analyzer for accurate scoring
4. **Brand Classification**: Identifies and categorizes smartphone brands
5. **Value Analysis**: Filters content discussing price and value
6. **Visualization**: Creates charts for easy interpretation

## Reddit Subreddits Analyzed

The project searches the following subreddits for smartphone discussions:
- r/android
- r/iphone
- r/samsung
- r/oneplus
- r/nothingtech
- r/redmi
- r/tecno
- r/infinix
- r/iQOO
- r/tech
- r/smartphones

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is open source and available under the [MIT License](LICENSE).

## Disclaimer

This project is for educational and research purposes. Please respect Reddit's terms of service and API usage guidelines when collecting data.

## Contact

For questions or suggestions, please open an issue in the repository.
