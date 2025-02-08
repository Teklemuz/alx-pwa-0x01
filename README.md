# alx-pwa-0x01

This project is designed to interact with **The Movie Database (TMDb) API v2**. 

## API Overview

The TMDb API provides access to movie, TV show, and actor data. It allows you to search for movies, retrieve details about specific movies, access trending content, and much more. The API is widely used for building movie and entertainment-related applications.

### Key Features:
- Search for movies and TV shows
- Retrieve detailed information about movies.
- Lists of trending movies. 
- Access movie and TV show images. 
- Filter content by genres, release dates, and ratings.

## API Version

The current version of the API is **v2**.

## Available Endpoints

Below are the main API endpoints available for use in version 2 of the TMDb API:

### 1. **GET /3/movie/popular**
   - **Description**: Fetches a list of popular movies.
   - **Example**: `/3/movie/popular?api_key=ac52910cec3481c93d9b349d&language=en-US&page=1`

### 2. **GET /3/movie/{movie_id}**
   - **Description**: Retrieves detailed information about a specific movie by ID.
   - **Example**: `/3/movie/550?api_key=ac52910cec3481c93d9b349d

### 3. **GET /3/movie/search**
   - **Description**: Search for movies by title or other filters.
   - **Example**: `/3/search/movie?api_key=ac52910cec3481c93d9b349d&query=Inception&language=en-US`

### 4. **GET /3/trending/movie/day**
   - **Description**: Get the list of trending movies for the current day.
   - **Example**: `/3/trending/movie/day?api_key=ac52910cec3481c93d9b349d

### 5. **GET /3/genre/movie/list**
   - **Description**: Retrieve a list of movie genres.
   - **Example**: `/3/genre/movie/list?api_key=ac52910cec3481c93d9b349d&language=en-US`

### 6. **GET /3/movie/{movie_id}/credits**
   - **Description**: Retrieve the cast and crew of a specific movie.
   - **Example**: `/3/movie/550/credits?api_key=ac52910cec3481c93d9b349d

### 7. **GET /3/movie/{movie_id}/images**
   - **Description**: Retrieve images for a specific movie (e.g., posters, backdrops).
   - **Example**: `/3/movie/550/images?api_key=ac52910cec3481c93d9b349d

## Request and Response Format

### Request Format:
Requests to the API should be made using the **GET** HTTP method. The request should include the necessary query parameters, such as the API key, language, and pagination parameters, and the endpoint path.

#### Example Request (for popular movies):
```bash
GET /3/movie/popular?api_key=ac52910cec3481c93d9b349d&language=en-US&page=1
### Response Format:
The API responds in JSON format, which includes the data you requested along with metadata about the request (e.g., page number, total results).

Example Response (for popular movies):{
  "page": 1,
  "results": [
    {
      "id": 550,
      "title": "Fight Club",
      "overview": "A young man with insomnia forms an underground fight club.",
      "release_date": "1999-10-15",
      "vote_average": 8.4,
      "poster_path": "/path_to_poster.jpg"
    },
    ...
  ],
  "total_pages": 500,
  "total_results": 10000
}
### API Key Authentication:
To authenticate requests to the TMDb API, you will need an API key. You can obtain an API key by creating an account and registering your app on TMDb's website. Once you have your API key, you include it in the request either via query parameter or HTTP header.

Example Authorization Header:
