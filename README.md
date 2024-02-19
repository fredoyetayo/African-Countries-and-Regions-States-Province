# African Countries and States JSON Data

This repository contains a JSON file listing all countries in Africa along with their constituent states/provinces. The data provides a structured way to link African states and regions to their parent country.

## Contents

The JSON file `africa.json` contains an array of country objects, each with the following structure:

```json
{
  "country": "Name of country", 
  "states": [
    "State/province name 1",
    "State/province name 2",  
    etc...
  ]
}
```

In total there are 54 African country objects, covering every internationally recognized sovereign state on the continent.

The `states` array contains the first-level administrative regions for that country. Most countries have provinces, regions, states, or other types of subdivisions. The exception is island nations like Cape Verde and Seychelles, which have subdivisions but no clearly defined states.

City-states like Djibouti are listed with their constituent districts. Disputed territories are not included.

## Usage Examples

The JSON data can be loaded into JavaScript using `require()`:

```js
const countries = require('./africa.json');
```

It can then be queried and manipulated like any other JavaScript object:

```js
// Get array of all countries
const countryNames = countries.map(country => country.country); 

// Get states for a specific country
const nigeriaStates = countries.find(c => c.country === 'Nigeria').states;

// Get number of states for each country
const statesByCountry = countries.map(c => ({
  country: c.country,
  states: c.states.length  
}));
```

The data can be used for:

- Populating country/state dropdowns in forms
- Building location-based applications
- Powering visualizations/charts about African geographies
- Looking up state-to-country metadata
- Seed data for databases of African locations

## Credits

This JSON data was compiled by Fred Oyetayo. Feel free to use it in your projects with attribution!

## Contributing

If you notice any issues with the data, please open an issue or submit a pull request with corrections. Contributions to improving the data are welcome!
