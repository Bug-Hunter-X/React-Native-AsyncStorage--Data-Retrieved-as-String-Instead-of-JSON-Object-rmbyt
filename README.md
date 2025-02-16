# React Native AsyncStorage: String vs. JSON Object Retrieval

This repository demonstrates a common yet often overlooked issue in React Native when using AsyncStorage to store and retrieve JSON data. The problem arises when the retrieved data is treated as a JSON object without proper parsing, leading to errors and unexpected behavior.

## The Problem

When storing a JSON object in AsyncStorage, it's essential to convert it into a string using `JSON.stringify`. However, upon retrieval, the data is a string and needs to be parsed back into a JSON object using `JSON.parse` before accessing its properties.  Failure to parse can lead to errors when attempting to access nested properties or cause your application to crash.

## Solution

The solution involves explicitly parsing the retrieved string data using `JSON.parse()` before utilizing it as a JSON object. This ensures that the data is correctly interpreted and prevents potential errors.

## How to Reproduce

1. Clone this repository.
2. Run the app on an Android emulator or iOS simulator.
3. Observe the console logs to see the error in the original example and successful retrieval in the solution.