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

name: C++ CI

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout code
      uses: actions/checkout@v2

    - name: Set up C++ environment
      uses: actions/setup-cpp@v1
      with:
        compiler: gcc

    - name: Install dependencies
      run: sudo apt-get install -y make g++

    - name: Build
      run: make

    - name: Run tests
      run: ./tests

## Llicència

GNU General Public License v3.0
