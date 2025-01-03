# Telegram Channel Data Analysis

This project involves extracting, cleaning, and analyzing data from a Telegram channel. The analysis includes clustering posts by topics, visualizing engagement metrics, and generating insights from the extracted data.

## Files and Directories

- `channel_data_clean.csv`: Cleaned data from the Telegram channel.
- `channel_data.csv`: Raw data extracted from the Telegram channel.
- `channel_messages.csv`: Additional message data.
- `data extraction.py`: Script to extract data from the Telegram channel. (not included for privacy reasons)
- `dendrogram`: Directory for dendrogram-related files.
- `main.ipynb`: Jupyter notebook for data analysis.


## Setup

### Install the Required Libraries

```bash
pip install -r requirements.txt
```

### Usage

1. Replace the following credentials in `data extraction.py` with your own:

   ```python
   api_id = 'your_api_id'
   api_hash = 'your_api_hash'
   channel_username = 'your_channel_username'
   ```

2. Run the `data extraction.py` script to extract data from the Telegram channel.

3. Use `main.ipynb` for data analysis and visualization. This notebook contains the code for cleaning, transforming, and visualizing the extracted data.

## Analysis Steps

### Import Libraries

Import necessary libraries such as pandas, numpy, matplotlib, and seaborn.

### Load Data

Load the extracted data from `channel_data.csv` into a pandas DataFrame.

### Data Preprocessing

- Aggregating certain rows, since each post update is recorded as a separate row.

### Analysis

Perform various analyses on the data, including:


- **Trend Analysis**
- **User Engagement Analysis**
- **Clustering**
- **BERTopic**
