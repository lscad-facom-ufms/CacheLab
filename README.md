# CacheLab: Enhancing Memory Hierarchy Learning Through Interactive Exploration

## Abou this project 
CacheLab is an open-source, web-based cache simulator. Designed to support both education and research, CacheLab provides an intuitive simulation environment for exploring cache mechanisms and advanced features for performance analysis. This simulator's primary purpose is to provide a detailed analysis of the behavior and performance of different cache-memory organizations. This analysis utilizes memory access patterns instrumented from real applications, enabling the exploration of the principles of spatial and temporal locality. The available functionalities and the user interface enable the simulator to serve as a didactic tool for teaching Computer Architecture. 

## Features
- **Realistic Input Data:** enables the evaluation of memory traces obtained from real applications, avoiding reliance on random or synthetic address simulations.
- **Customizable Cache Design:** allows users to configure set-associative caches with one or multiple levels, customizing parameters such as block size, number of blocks, associativity, and replacement policies for each level.
- **Configurable Performance Metrics:** supports the definition of performance parameters, including hit time and miss penalty, enabling detailed performance analysis.
## Memory Traces
- A memory trace is a sequence of all events that involve memory accesses during the execution of a program. These events include information such as the addresses accessed, the operation mode (read or write), the data being transferred, and the address of the instruction that triggered the operation.

# Running locally

This project was bootstrapped with [Vite](https://vite.dev/guide/).

## Installing dependencies

This project uses NPM as the package manager, so make sure you have it installed on your machine before proceeding.

Run `npm install` to install all dependencies.

## Available Scripts

In the project directory, you can run:

### `npm run dev`

Runs the app in the development mode.\
Open [http://localhost:5173](http://localhost:5173) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm run test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://vitest.dev/guide/) for more information.

### `npm run build`

Builds the app for production to the `dist` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

## Learn More

You can learn more in the [Vite documentation](https://vite.dev/guide/).

To learn React, check out the [React documentation](https://reactjs.org/).
