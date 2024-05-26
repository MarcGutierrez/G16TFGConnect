# TFGConnect
TFGConnect repository

## Taula de Continguts
- [Instal·lació](#instal·lació)
- [Ús](#ús)
- [Contribució](#contribució)
- [GitHub Actions](#github-actions)
- [Llicència](#llicència)

## Instal·lació

1. Clonar el repositori:
    ```sh
    git clone https://github.com/nom-usuari/nom-repositori.git
    ```
2. Entrar al directori del projecte:
    ```sh
    cd nom-repositori
    ```
3. Instal·lar les dependències:
    ```sh
    npm install
    ```

## Ús

Proporciona exemples i instruccions sobre com utilitzar el projecte. Per exemple:

  ```sh
  npm start
  ```

## Contribució

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
