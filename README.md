# TFGConnect
TFGConnect repository

## Taula de Continguts
- [Installation](#installation)
- [Use](#use)
- [Contribution](#contribution)
- [GitHub Actions](#github-actions)
- [License](#license)

## Installation

1. Clone the repository:
    ```sh
    git clone https://github.com/MarcGutiérrez/G16TFGConnect.git
    ```
2. Get in the repository folder:
    ```sh
    cd G16TFGConnect
    ```
3. Install the dependencies (currently none):
    ```sh
    npm install
    ```

## Use

Currently there are no uses. This is only a placeholder.

  ```sh
  npm start
  ```

## Contribution

We are group 16.
# Group members
Judit Viladecans

Marc Gutiérrez

Sergi García

Cristina Ortega

Mar Climente

Biel Solà

Omar Hamze

## Github Actions

name: Java CI

on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout repository
      uses: actions/checkout@v2

    - name: Set up JDK 11
      uses: actions/setup-java@v3
      with:
        distribution: 'adopt'
        java-version: '11'

    - name: Build with Maven
      run: mvn clean install

    - name: Run tests with Maven
      run: mvn test

## Llicència

GNU General Public License v3.0
