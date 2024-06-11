# YouTube-Sentiment-Analyzer

## Project Description
**YouTube Sentiment Analyzer** is an interactive application designed to fetch and analyze YouTube video data based on user-defined subtopics. Utilizing the power of natural language processing and sentiment analysis, this project provides insights into viewer opinions and trends. Key features include the ability to filter videos by date or popularity, detailed video statistics, and comprehensive sentiment analysis of video comments, presented through informative word clouds and sentiment metrics.

## Key Features
1. **Subtopic Search:** Input a subtopic to fetch related YouTube videos.
2. **Video Filtering:** Option to filter videos by date range or most viewed.
3. **Comment Analysis:** Fetches and analyzes a specified number of comments per video.
4. **Sentiment Analysis:** Uses TextBlob to determine the sentiment polarity of comments.
5. **Word Clouds:** Generates word clouds for all comments, positive comments, and negative comments.
6. **Sentiment Metrics:** Displays overall sentiment and detailed statistics for positive and negative comments.
7. **Detailed Video Statistics:** Provides video-specific details including title, channel, views, likes, dislikes, comments, and publication date.

## Data Science Techniques

### 1. Data Collection and Integration:

- **API Usage:** The code uses the YouTube Data API to fetch video and comment data. This involves sending requests to an external API, handling responses, and integrating the fetched data for further analysis.

### 2.Text Processing and Natural Language Processing (NLP):

- **Tokenization:** The code uses the SinhalaTokenizer to break down Sinhala text comments into individual tokens (words). Tokenization is a fundamental NLP technique used for text processing.
- **Sentiment Analysis:** The TextBlob library is used to perform sentiment analysis on comments. This involves determining the polarity (positive or negative sentiment) of each comment.
- **Feature Extraction:** Extracting meaningful features (tokens and sentiments) from the text data for further analysis.

### 3. Data Visualization:

- **Word Clouds:** The code generates word clouds to visually represent the frequency of words in comments, as well as separately for positive and negative comments. Word clouds help in identifying common themes and keywords.
- **Matplotlib:** Matplotlib is used for creating the word cloud visualizations and embedding them in the Tkinter GUI.

### 4. Graphical User Interface (GUI):

- **Tkinter:** The Tkinter library is used to create a graphical user interface that allows users to input parameters, fetch data, and view results. While primarily a UI tool, its integration with data visualization tools (like Matplotlib) makes it relevant in presenting data science results interactively.

### 5. Sentiment Calculation and Aggregation:

- **Overall Sentiment Calculation:** The code calculates the overall sentiment score by aggregating positive and negative sentiment counts and displaying the result in a user-friendly manner.

### 6. Date Handling:

- **Date Filtering:** The code allows filtering videos by date using DateEntry widgets from the tkcalendar library. Handling date inputs and filtering data based on date ranges is a common data science task.

## How Text Processing and Natural Language Processing (NLP) Work in This Project

### 1. Fetching and Preprocessing Comments:
#### Fetching Comments:
- The application utilizes the YouTube Data API to search for videos and fetch comments.
- Users specify a subtopic, number of videos, and number of comments per video.
- The API retrieves video details and associated comments, which are then stored for further analysis.

#### Preprocessing Comments:
- **Tokenization:** The process of breaking down text into smaller units (tokens), typically words or phrases.
    - In this project, the SinhalaTokenizer from the Sinling library is used to handle Sinhala text, which may have unique linguistic structures and characters compared to English.
    - Each comment is passed through the tokenizer to produce a list of individual words or tokens.
    - Tokenization helps in transforming raw text into a structured format suitable for analysis.

### 2. Sentiment Analysis:
#### Analyzing Comments:
- **TextBlob Sentiment Analysis:**
    - TextBlob is a Python library for processing textual data. It provides a simple API for diving into common natural language processing (NLP) tasks such as part-of-speech tagging, noun phrase extraction, sentiment analysis, and more.
    - For each tokenized comment, TextBlob analyzes the text and assigns a polarity score. The polarity score ranges from -1 (negative) to +1 (positive), with 0 being neutral.
    - **Sentiment analysis using TextBlob involves:**
         -  **Polarity Detection:** Determines the overall sentiment of the comment. A positive score indicates a positive sentiment, a negative score indicates a negative sentiment, and a score close to zero indicates a neutral sentiment.
         -  **Subjectivity Detection:** Measures how subjective or objective the text is. However, in this project, we primarily focus on polarity for sentiment classification.
#### Classifying Comments:
- Based on the polarity score:
    - Comments with a positive polarity (>0) are classified as positive.
    - Comments with a negative polarity (<0) are classified as negative.
    - Neutral comments (polarity ≈ 0) are typically less emphasized in visualization but can be stored for completeness.
#### Storing Results:
- Positive and negative comments are stored separately to facilitate detailed analysis and visualization.
- The counts of positive and negative comments are tracked to compute the overall sentiment distribution.

### 3. Visualization:
#### Generating Word Clouds:
