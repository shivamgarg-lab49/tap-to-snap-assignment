# Android Project Assignment

Welcome to the Android project assignment! We're excited to have you work on this task. This document outlines the assignment and provides instructions on how to complete it.

## Assignment Overview

The goal of this assignment is to build a simple Android application that demonstrates your understanding of key Android development concepts, including the latest technologies and best practices. You'll be tasked with creating a basic Android app that includes specific features and functionalities, utilizing modern Android libraries and architectural patterns.

## Task Description

### Project Setup
1. Clone this repository to your local machine.
2. Open the project in Android Studio.

### Assignment Requirements
Your task is to create an Android application with the following features, incorporating the latest Android technologies:

1. **User Interface (UI):**
   - **Screen 1 (Splash Screen):**
     - Display a splash screen with a "Let's Go" button.
     - Design the splash screen based on the provided screenshots for reference.
   - **Screen 2 (Main Screen):**
     - Display the list of image labels received from the API endpoint.
     - Navigate to this screen when the "Let's Go" button is clicked on the splash screen.
     - Utilize RecyclerView or similar components for displaying the list in a grid.
     - Main screen drawables are included in the code itself.
     - The number of grid items should be equal to the number of image labels received.
     - **On each grid item click, perform the following steps:**
        1. Open the camera application and capture a photo.
        2. Convert the image data into a Base64 string.
        3. Invoke the second endpoint by passing the image label and the selected image Base64 string.
        4. Display a progress indicator within the grid item.
        5. If the API returns "matched" as "false" or encounters an error, display a "Try Again" message with a red rounded corner shape.
        6. If the API returns "matched" as "true", display a green rounded corner shape.

2. **Functionality:**
   - Implement asynchronous operations using Coroutines and Flows for handling background tasks and asynchronous data streams.
   - Utilize Retrofit for making network requests and fetching data from a RESTful API.
   - Implement dependency injection using Hilt for managing app-level dependencies.
   - Implement ViewModel and Flows from the Android Architecture Components library to manage UI-related data and lifecycle.
   - **Winning Rule:**
      - Make all grid boxes green within a time frame.
      - Stop the timer if the task is completed early.
      - Display an alert dialog saying "Congratulations!! You've won the game!" with two options: "Exit" to close the app and "Restart" to restart the application and reset all previous state.
   - **Losing Rule:**
      - If you fail to make all boxes green, you will lose the game within a time frame.
      - Display an alert dialog saying "You\'ve run out of time, Better luck next time!" with two options: "Exit" to close the app and "Restart" to restart the application and reset all previous state.

3. **Additional Requirements:**
   - Adhere to the Model-View-ViewModel (MVVM) architectural pattern for separating concerns and promoting maintainability.
   - Ensure the application is responsive and works across different screen sizes and orientations.
   - Use modern Android design guidelines and material components for designing the user interface.
  
4. **Testing:**
   - Good to have test case for view models 
   - Test ViewModel classes using JUnit and Mockito to ensure proper behavior.

### Endpoint Information
You'll need to utilize the following endpoints:
1. **First Endpoint (To fetch image labels):**
   - **Endpoint:** [https://veritask.vercel.app/api/images](https://veritask.vercel.app/api/images)
   - **Description:** This endpoint provides an array of imageLabel strings. You should call this endpoint when the "Let's Go" button is clicked on the splash screen, and pass the received image labels to the main screen.
2. **Second Endpoint (For image data validation):**
   - **Endpoint:** [https://veritask.vercel.app/api/images](https://veritask.vercel.app/api/images)
   - **Description:** This endpoint expects a POST request with JSON body containing the image label and Base64-encoded image data. The response will contain the validation result, indicating whether the image data matched the provided label.
   - Sample Request Body {"imageLabel":"landscape","image":"VGhpcyBpcyBhIHRlc3Q="}


### Screenshots and Video
For your reference, we have provided screenshots and a video demonstration of the application's functionality. You can find them [here](samples/screenshots).

### Postman collection 
For your reference, we have provided postman collection for above API's. You can find them [here](samples/postman-collection).

### Additional Notes
- Feel free to explore additional libraries or frameworks that complement the mentioned technologies.
- Ensure your code follows best practices and is well-documented.

## Resources
- [Android Developer Documentation](https://developer.android.com/docs)
- [Android Studio Guide](https://developer.android.com/studio/intro)
- [GitHub Guides](https://guides.github.com/)

We look forward to seeing your work!

Happy coding!
