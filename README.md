# Brief Synopsis of Weather App Development
This project involved the development of a dynamic weather application built on the Wix platform, leveraging Velo (Wix's JavaScript) for front-end logic and utilizing a backend web module (openWeatherAPI.web) to interact with the OpenWeatherMap API. The primary goal was to create a user-friendly interface that allows users to view current weather conditions and a 5-day forecast for a specified location, with the added functionality of saving a favorite location.
Key Features and Implementation:
Real-time Weather Data Retrieval: The app uses the getCurrentWeather and getForecast functions from the backend module to fetch live weather data based on user-inputted or previously saved locations and selected units (Celsius or Fahrenheit).
Dynamic UI Updates: Upon fetching data, the application dynamically updates various UI elements, including temperature, city name, weather description, min/max temperatures, wind speed, humidity, and weather icons. Loading animations provide visual feedback during the data fetching process.
Location Input and Submission: Users can enter a city name via an input field and trigger a weather data update by clicking a submit button. The entered location is encoded for safe URL usage. A default location ("New York") is used if the input is empty.
Unit Switching: Dedicated buttons allow users to switch between Celsius and Fahrenheit, triggering a re-fetch and re-display of the weather data in the selected unit.
Favorite Location Saving: A checkbox allows users to save the currently viewed location and unit as their favorite. This information is stored locally in the user's browser using wix-storage.local.
Loading of Favorite Settings: On page load, the app checks wix-storage.local for previously saved favorite settings. If found, it automatically loads these settings and displays the weather for the favorite location and unit. A "Delete Favorite" button allows users to clear these saved settings.
Error Handling: The application includes basic error handling using try...catch blocks to gracefully navigate the user to an error page (/error) if issues arise during API calls.
Forecast Display: A repeater element is used to display the 5-day forecast. The onItemReady function dynamically populates each forecast item with the day of the week, minimum and maximum temperatures for the day, and a corresponding weather icon.
Unique Item IDs: The uuidv4() library is used to generate unique IDs for the forecast repeater items, ensuring proper rendering and data binding.
Navigation: Buttons are implemented for navigating back to the homepage (/) and potentially to an error page.
How I Believe This Helped:
This project demonstrates my ability to:
Integrate with external APIs: Successfully fetched and utilized data from the OpenWeatherMap API to provide real-time information.
Develop dynamic front-end applications: Used JavaScript and the Wix Velo framework to create an interactive user interface that updates based on user actions and API responses.
Manage asynchronous operations: Effectively used async/await to handle API calls and ensure the UI updates correctly after data retrieval.
Implement local data storage: Utilized wix-storage.local to persist user preferences (favorite location and unit), improving user experience by remembering their settings.
Handle user input and events: Implemented event listeners for button clicks and checkbox changes to trigger application logic.
Display data in structured formats: Used repeater elements to present the forecast data in an organized and user-friendly manner.
Implement basic error handling: Included mechanisms to navigate users to an error page in case of API failures, contributing to a more robust application.
Understand UI/UX principles: Incorporated loading animations to provide feedback to the user during data fetching, enhancing the perceived performance and user experience.
This weather app showcases my ability to build a functional and interactive web application on the Wix platform, integrating external services and managing client-side state to deliver a valuable user experience.
