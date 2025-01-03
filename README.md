# Telegram Channel Data Analysis

This project involves extracting, cleaning, and analyzing data from my personal Telegram channel about fitness: https://t.me/yavgym. The analysis includes clustering posts by topics, visualizing engagement metrics, and generating insights from the extracted data.

## Files and Directories

- `channel_data_clean.csv`: Cleaned data from the Telegram channel.
- `channel_data.csv`: Raw data extracted from the Telegram channel.
- `channel_messages.csv`: Additional message data.
- `data extraction.py`: Script to extract data from the Telegram channel. (not included for privacy reasons)
- `dendrogram`: Directory for dendrogram-related files.
- `main.ipynb`: Jupyter notebook for data analysis.

### Steps
#### 1️⃣ Data Extraction
Using Python and the `telethon` library, I extracted posts, views, comments, reactions, and whether the posts contained any media (e.g., photos, videos). This step was challenging but rewarding—I managed to get all the key statistics for each post while maintaining clean and structured data.

#### 2️⃣ Data Cleaning and Preprocessing
The raw data had many duplicates and rows with minimal differences in timestamps. To fix this:
- I combined rows where posts were made within 5 minutes of each other, aggregating their reactions, media types, and text while keeping the maximum views and comments.
- This approach ensured meaningful aggregation and reduced redundancy.

#### 3️⃣ Exploratory Data Analysis (EDA)
I analyzed key metrics like:
- **Post Engagement**: Views, comments, and reactions to identify which posts resonated most with my audience.
- **Content Type Analysis**: Comparing engagement for posts with text, photos, or videos to see what drives interaction.

#### 4️⃣ Data Visualization
To make the insights actionable, I created visualizations:
- **Time-Series Analysis** of engagement trends over time.
- **Bar Charts** showing top-performing posts based on views, comments, and reactions.
- **Word Clouds** to highlight the most frequent words and phrases in my posts.

#### 5️⃣ Clustering Step
Performed topic clustering to group posts by similarities:
- Explored clustering with methods like **KMeans and Hierarchical Clustering**.
- Used metrics like **elbow method and silhouette scores** to evaluate clustering performance.

#### 6️⃣ BERTopic Model
Implemented BERTopic for topic modeling:
- Extracted coherent topics from posts ("Food&Recipes", "Sport&Fitness", "Lifestyle").
- Visualized document-topic relationships using tools like `visualize_documents`.
- Identified dominant topics for each post.

#### 7️⃣ Engagement Analysis
Analyzed engagement metrics (e.g., views, reactions, comments) by topics:
- Grouped data by topics and calculated average engagement.
- Created visualizations (e.g., bar charts) to compare engagement across topics.


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
