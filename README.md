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
