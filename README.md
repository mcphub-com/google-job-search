# Aigeon AI Google Job Search

## Project Description

Aigeon AI Google Job Search is a Python-based server application designed to facilitate the scraping of job listings from Google Jobs using the SerpApi service. This application provides a robust interface for querying job data with various customizable parameters, allowing users to tailor their search results according to specific needs such as location, language, and more.

## Features Overview

- **Customizable Job Search**: The application allows users to perform job searches with a variety of parameters, making it flexible for different search requirements.
- **Integration with SerpApi**: Utilizes the SerpApi service to fetch Google Jobs data, ensuring reliable and up-to-date results.
- **Environment Configuration**: Uses environment variables for sensitive data management, enhancing security.
- **Asynchronous and Cached Searches**: Supports both synchronous and asynchronous search requests, as well as cached results to optimize performance and reduce API usage.

## Main Features and Functionality

1. **Search Job Functionality**: The core feature of the application is its ability to perform job searches on Google Jobs through the SerpApi. Users can customize their search queries with a wide range of parameters.
2. **Parameter Customization**: The application supports numerous parameters such as location, language, search radius, and more, allowing for highly specific job searches.
3. **Response Handling**: The application processes the API response and returns the job search results in JSON format, making it easy to integrate with other systems or applications.
4. **Server Execution**: The application runs as a server using the FastMCP framework, listening for incoming requests and processing them accordingly.

## Main Functions Description

### `search_job`

This function is the primary tool for executing a job search query on Google Jobs using the SerpApi. It accepts several parameters to customize the search:

- **q**: (str) The search query string for the job search.
- **location**: (Union[str, None]) Specifies the location from which the search should originate. If omitted, the search may default to the proxy's location.
- **uule**: (Union[str, None]) Google encoded location for the search. Cannot be used with the `location` parameter.
- **google_domain**: (Union[str, None]) The Google domain to use for the search, defaulting to google.com.
- **gl**: (Union[str, None]) Country code for the search, e.g., 'us' for the United States.
- **hl**: (Union[str, None]) Language code for the search, e.g., 'en' for English.
- **next_page_token**: (Union[int, None]) Token for retrieving the next page of results.
- **lrad**: (Union[float, None]) Search radius in kilometers.
- **uds**: (Union[str, None]) Filter string provided by Google for search refinement.
- **no_cache**: (Union[bool, None]) Determines whether to force a fresh search or allow cached results.
- **aasync**: (Union[bool, None]) Determines whether the search is submitted asynchronously.

The function constructs a payload with the provided parameters, sends a GET request to the SerpApi, and returns the JSON response containing the job search results.

---

This README provides a comprehensive overview of the Aigeon AI Google Job Search application, detailing its features, functionality, and how to utilize its main functions effectively.