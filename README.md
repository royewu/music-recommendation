# Cross-Platform Music Recommendation System

This project demonstrates the integration of heterogeneous music datasets from Spotify and Apple Music to enable cross-platform song and artist recommendations. By leveraging Python, SQL, and data cleaning techniques, the system identifies similar songs based on genre, artist, and popularity data. 

## Introduction

Music streaming services often operate independently, limiting users from receiving integrated recommendations across platforms. This project addresses this gap by combining data from Spotify and Apple Music to generate cross-platform recommendations.

## Features

- **Cross-Platform Recommendations**: Leverages datasets from Spotify and Apple Music to provide integrated suggestions
- **Personalized Results**: Recommendations tailored to the user's top 50 recently played tracks on Spotify
- **Data Cleaning and Standardization**: Streamlined genre labels and column names to ensure compatibility across platforms
- **Efficient SQL Querying**: Supports seamless database operations for recommendations
- **Exportable Results**: Outputs user-specific recommendations in CSV format for accessibility

## Dataset Details

- **Spotify Data**: Over 100,000 tracks with genre and popularity metrics
- **Apple Music Data**: 10,000 tracks categorized by genre and artist
- **User Data**: Top 50 recently played tracks on Spotify

All datasets were integrated into an SQLite database, allowing efficient cross-platform querying

## Methods

1. **Data Cleaning and Integration**:
   - Removed irrelevant columns and handled null values
   - Standardized column names (e.g., "track_name" → "song", "artists" → "artist")
   - Simplified genre labels for consistency

2. **Database Setup**:
   - Separate tables for Spotify, Apple Music, and user-specific data
   - Unified schema to facilitate cross-platform recommendations

3. **Recommendation Logic**:
   - **Songs**: Matched tracks based on genre similarity, artist diversity, and Spotify popularity scores
   - **Artists**: Recommended popular artists from the user's preferred genres

## Results

- Generated cross-platform recommendations for the user's top three songs
- Identified similar tracks and artists based on genre, artist, and popularity metrics
- Exported results to CSV files for easy access

![musicrec_results](https://github.com/user-attachments/assets/91fe61ec-0edf-4a54-bd9e-adde132cbca1)

## Challenges

- **Dataset Imbalance**: Spotify's dataset size significantly exceeded Apple Music's, leading to uneven insights
- **Genre Simplification**: Simplifying genres occasionally resulted in less accurate recommendations
- **Platform-Specific Constraints**: Apple Music lacked popularity metrics, limiting recommendation depth

## Future Work

- Address dataset imbalances by sourcing more Apple Music data
- Refine genre matching for greater recommendation accuracy
- Incorporate advanced machine learning models to enhance predictive capabilities
- Expand API usage for dynamic and scalable data retrieval

## Technologies Used

- **Python**: For data preprocessing and genre simplification
- **SQL**: For database setup and querying
- **SQLite**: To manage integrated datasets
- **Spotify API**: For user-specific data collection

## How to Run

1. Clone the repository
2. Ensure all dependencies are installed (Python 3.x, SQLite)
3. Populate the database with the provided datasets
4. Execute the recommendation script to generate results
5. View the output recommendations in the exported CSV files
