# Workshop-React-Native

Hello everyone and welcome :)


This workshop is an introduction to React Native using [expo](https://docs.expo.dev/) where we will learning how to fetch data from and an API and displaying its content! (I know, exciting).


For that, we will be creating a weather app with the [openweatherapi](https://openweathermap.org/api), which is a provider of highly recognisable weather products that make working with the weather data a way easier. 

Skills you will acquire:

- Introduction to React Native
- Introduction to expo
- How to use openweathermap API
- Integrating openweathermap with react native expo
- Search Weather Data of different cities using react native expo
- Component management
- Get information like, sunrise time, sunset time, humidity, windspeed, pressure of any city in the world using react native expo and openweathermap
- Amazing Weather App With decent UI using react native

Without further ado, let's get started with the installations!

## Installations

  For this project you will only need to install NodeJs and expo if you don't have them already!

  <details>
    <summary>NodeJS</summary>

  First make sure you have npm installed using ```node -v```, if it's not installed already, follow this!

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
 4- Check that the install was successful by querying node for its version number, make sure you at least have the ```7.24.0```
  ```
 sudo apt install npm
  ```

  </details>

  <details>
    <summary>Expo</summary>

  If it's already installed, make sure you at least have the ```v16.10.0```

  Let's now start by installing expo! 
  ```
  sudo npm install -g expo-cli
  ```

  Now create a new expo project named ```workshop-weather-app```
  ```
  expo init workshop-weather-app
  ```

  Enter your project ```cd workshop-weather-app```, and then run the expo server
  ```
  expo start
  ```

  Now you probably have a QR code generated, all you need to do is:

  - Make sure you're on the same network as your phone

  - Install the Expo Go app on your phone

  - Set up your account

  - Open your camera app

  - Scan the QR code and open it

  Now you're all set to get started with the project!!!
  
  </details>

  </details>
</details>

## Activities

  <details>
    <summary>Activity 1</summary>

We're going to use the [openweatherapi](https://openweathermap.org/api) API, so sign up to the website and copy your generated key [here](https://home.openweathermap.org/api_keys) 

This is the API we're going to use: 
```
"https://api.openweathermap.org/data/2.5/weather?q={City name}&appid={API key}"
```

Now, let's create a new folder called src, and inside it, create a new file called ```WeatherFetch.js```


And now try to use the API to fetch the weather data with a function named ```fetchWeatherData```, that takes ```cityName``` as parameter that represents the city we're looking for and returns the weather data for that city.

This is what the main function will look like:

```
API_KEY = 'your api key'

const WeatherFetch = () => {
  
  const fetchWeatherData = async (cityName) => {
    const response = await fetch(`https://api.openweathermap.org/data/2.5/weather?q=${cityName}&appid=${API_KEY}&units=metric`);
    //your code here
  }
  return (
    <View>
        <Text>In WeatherFetch</Text>
    </View>
  )
}
```
  </details>

  <details>
    <summary>Activity 2</summary>

Now that we can have fetch through our API, we will create a new file called ```WeatherInfo.js``` that will display each information that you want to display from that API.

Make sure to check the app on your phone and that it displays the content you're looking for!

This is what the code will look like:

```
const WeatherInfo = ({ weatherData }) => {

    const { 
        name,
        visibility,
        main: { temp, feels_like, temp_min, temp_max, pressure, humidity },
        ...
    } = weatherData;

  return () {
    <SafeAreaView>
        //data you want to display
    </SafeAreaView>
  }
}
```

Don't forget to call this component in the ```WeatherFetch``` component! :) 

  </details>

  <details>
    <summary>Activity 3</summary>

Now create a search bar component in a file called ```WeatherSearch``` that takes as parameters ```fetchWeatherData```.

This component will allow the user to search for a city and display the weather data of that specified city. 

For that, create a search bar and a button, and when the user presses the button, it should display the weather data for that city.

You can use the onPress event, and call the ```fetchWeatherData``` function and display the data.

  </details>

  <details>
    <summary>Activity 4</summary>

Now that you have an app, fully functional, you can style using any UI Component library you want, or you can use the default ones that expo provides.

I suggest you to use the [Tailwind](https://www.nativewind.dev/quick-starts/expo) library, which is a utility-first CSS framework for rapidly building custom designs.

  </details>

</details>