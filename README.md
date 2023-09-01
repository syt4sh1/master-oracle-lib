# master-oracle-lib

## Description

master-oracle-lib is a JavaScript library for interacting with the Master Oracle API. It provides a convenient way to fetch data from the Master Oracle platform, making it easy for developers to integrate oracle data into their applications.

## Features

- Fetch data from the Master Oracle API.
- Easy-to-use and customizable.

## Installation

Install the package using npm or yarn:

```
npm install master-oracle-lib
or
yarn add master-oracle-lib
```
## Usage
```
const MasterOracleLib = require('master-oracle-lib');

// Initialize with your API key
const apiKey = 'your-api-key';
const masterOracle = new MasterOracleLib(apiKey);

// Example usage to fetch data
const symbol = 'BTC/USD';
const timeframe = '1h';

masterOracle.fetchData(symbol, timeframe)
  .then(data => {
    console.log(data);
  })
  .catch(error => {
    console.error(error);
  });
```
## API Documentation
`new MasterOracleLib(apiKey)`
`apiKey (string, required):` Your Master Oracle API key.
`masterOracle.fetchData(symbol, timeframe)`
`symbol (string, required):` The symbol for the data you want to fetch (e.g., 'BTC/USD').
`timeframe (string, required):` The timeframe for the data (e.g., '1h').
Returns a Promise that resolves to the fetched data or rejects with an error.
