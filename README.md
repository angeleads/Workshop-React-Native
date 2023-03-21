# Workshop-React-Native

Hello everyone and welcome :)


This workshop is an introduction to React Native using [expo](https://docs.expo.dev/) where we will learning how to fetch data from and an API and displaying its content! (I know, exciting).


For that, we will be creating a weather app with the [openweatherapi](https://openweathermap.org/api), which is a provider of highly recognisable weather products that make working with the weather data a way easier. 


Without further ado, let's get started with the installations!

## Installations

  First make sure you have npm installed using ```node -v```, if it's not installed already, follow this!

  <details>
    <summary>NodeJS</summary>


  1- To get this version, you can use the apt package manager. Refresh your local package index first:
  ```
  sudo apt update
  ```
  2- Then install Node.js:
  ```
  sudo apt install nodejs
  ```
  3- Check that the install was successful by querying node for its version number, make sure you at least have the ```v16.10.0```
  ```
  node -v
  ```
  </details>

  If it's already installed, make sure you at least have the ```v16.10.0```

  Let's now start by installing expo! 
  ```
  sudo npm install --global
  ```

  Now create a new expo project
  ```
  npx workshop-weather-app --template
  ```

  Enter your project ```cd workshop-weather-app```, and then run the expo server
  ```
  expo start
  ```

  Now you probably have a QR code generated, all you need to do is:

  - Install the Expo Go app on your phone

  - Set up your account

  - Open your camera app

  - Scan the QR code and open it

  Now you're all set to get started with the project!!!

  </details>

## Activities

### Activity 1

We're going to use the [openweatherapi](https://openweathermap.org/api) API, so sign up to the website and copy your generated key [here](https://home.openweathermap.org/api_keys) 

Now, let's create a new folder called src, and inside it, create a new file called ```api.js```

And now try to use the API to fetch the weather data with a function named ```fetchWeatherData```, that takes a city as a parameter and returns the weather data for that city.

### Activity 2

Now that we can have fetch through our api, we will create a new file called ```WeatherInfo.js``` that will display each information that you want to display from the API. 

Make sure to check the app on your phone and that it displays the content you're looking for!

### Activity 3

Now create a search bar component, that will allow the user to search for a city and display the weather data for that city.

For that, create a search bar an a button, and when the user presses the button, it should display the weather data for the city that the user entered.

You can use the onPress event, and call the ```fetchWeatherData``` function and display the data.

### Activity 4

Now that you have an app, fully functional, you can style using any UI Component library you want, or you can use the default ones that expo provides.

</details>