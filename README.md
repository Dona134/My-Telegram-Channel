# My-Telegram-Channel

## Project Overview
This project aims to analyze engagement metrics (comments and reactions) across different content topics. Using clustering and BERTopic modeling, we categorized posts into meaningful topics and visualized their engagement performance to derive actionable insights.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Preprocessing](#data-preprocessing)
- [Topic Modeling](#topic-modeling)
- [Engagement Analysis](#engagement-analysis)
- [Visualizations](#visualizations)
- [Insights](#insights)
- [Setup and Usage](#setup-and-usage)

## Data Preprocessing
1. **Data Cleaning:**
   - Removed missing or irrelevant data points.
   - Processed text data to extract meaningful phrases.
2. **Feature Extraction:**
   - Tokenized posts to generate noun-based features.
   - Used TF-IDF for vectorization.

## Topic Modeling
- Applied **BERTopic** for unsupervised topic modeling.
- Identified three primary topics:
  1. **Food and Recipes**
  2. **Lifestyle**
  3. **Sport and Fitness**

## Engagement Analysis
- Engagement metrics include:
  - **Total Reactions:** Sum of all reactions to a post.
  - **Comments:** Number of comments on a post.
- Metrics were averaged across the identified topics.

## Visualizations
- **Hierarchical Clustering Dendrogram:** Displayed topic similarity based on embeddings.
- **Engagement Bar Chart:** Compared average engagement metrics across topics.

## Insights
1. **Sport and Fitness** posts receive the highest total reactions, indicating strong audience resonance.
2. **Lifestyle** posts generate more comments, fostering discussion and interaction.
3. **Food and Recipes** posts attract moderate reactions but could be improved by encouraging more active participation.

## Setup and Usage
### Prerequisites
- Python 3.8+
- Required Libraries:
  - `pandas`
  - `matplotlib`
  - `bertopic`
  - `scikit-learn`

### Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Project
1. Preprocess the dataset and generate topics:
   ```python
   python preprocess_data.py
   ```
2. Perform engagement analysis:
   ```python
   python analyze_engagement.py
   ```
3. Visualize results:
   ```python
   python visualize_results.py
   ```

## Contributions
Feel free to contribute by submitting issues or pull requests to enhance the analysis.

## License
This project is licensed under the MIT License. See the LICENSE file for more details.

channel_data_clean.csv: Cleaned data from the Telegram channel.
channel_data.csv: Raw data extracted from the Telegram channel.
channel_messages.csv: Additional message data.
data extraction.py: Script to extract data from the Telegram channel.
dendrogram: Directory for dendrogram-related files.
fasttext_wheel-0.9.2-cp312-cp312-win_amd64.whl: FastText library wheel file.
main.ipynb: Jupyter notebook for data analysis.
