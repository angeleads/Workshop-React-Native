# Workshop-React-Native

Hello everyone and welcome :)


This workshop is an introduction to React Native using [expo](https://docs.expo.dev/) where we will learning how to fetch data from and an API and displaying its content! (I know, exciting)
For that, we will be creating a weather app with the [openweatherapi](https://openweathermap.org/api), which is a provider of highly recognisable weather products that make working with the weather data a way easier. 


Without further ado, let's get started with the installations!

## Installation

<details>
  <summary>Ubuntu:</summary>

  <details>
    <summary>NodeJS</summary>

  First make sure you have npm installed using ```node -v```, if it's installed already, follow this!

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

  Let's now start by installing expo! 
  ```
  sudo npm install --global
  ```

  Now create a new expo project
  ```
  npx weather-app --template
  ```

  Enter your project ```cd weather-app```, and then run the expo server
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

<details>
  <summary>Activity 1</summary>
    We're going to use the [openweatherapi](https://openweathermap.org/api) API, so sign up to the website and copy your generated key [here](https://home.openweathermap.org/api_keys) 

    Let's create a new folder called src, and inside it, create a new file called ```api.js```
    And now try to use the API to fetch the weather data.
<details>