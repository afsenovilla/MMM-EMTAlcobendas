# Module: MMM-EMTAlcobendas
This [MagicMirror](https://github.com/MichMich/MagicMirror) module displays information about estimations for bus stops in the city of Alcobendas (Madrid-Spain). The service is provided by EMT Madrid. Supports **English** (*en*), **Spanish** (*es*) and **Catalan** (*ca*).

<center><img src="https://theraulxp.es/legacy/emt_magicmirror.png" alt="Module screen" width="400"></center>

## Dependencies
- An installation of [MagicMirror<sup>2</sup>](https://github.com/MichMich/MagicMirror)
- [xml2js](https://www.npmjs.com/package/xml2js)

## Installation

Navigate into your MagicMirror's `modules` folder:
```
cd ~/MagicMirror/modules
```

Clone this repository:
```
git clone https://github.com/afsenovilla/MMM-EMTAlcobendas
```

Navigate to the new `MMM-EMTAlcobendas` folder and install the node dependencies.
```
npm install
```

Configure the module in your `config.js` file.

## Find your stop number
To configure this module, you will need a stop number, and, optionally, the line number which you want to get information about. The stop number can be found by looking for it at EMT Madrid's website or Google Maps.  


[EMT Madrid's website]([https://www.emtmadrid.es/EMTBUS/MiBus])


## Using the module

To use this module, add it to the modules array in the `config/config.js` file. 

```javascript
modules: [
  {
    module: 'MMM-EMTAlcobendas',
    position: 'top_left',
    header: 'My bus stop',
    config: {
      stopNumber: 683,
      stopLine: null,
      updateInterval: 10
    }
  },
]
```

## Configuration options

The following properties can be configured:

| Option                       | Description
| ---------------------------- | -----------
| `stopNumber`                 | ID number of the bus stop.<br><br>**Required**<br>**Value type:** `Integer`<br>**Default value:** `683`
| `stopLine`                 | Bus line to filter, ignoring other lines that share the same stop.<br><br>**Value type:** `Integer`<br>**Default value:** ` null ` (Show every line from the stop)
| `updateInterval`             | Time (in seconds) to wait before refreshing the data from the API.<br><br>**Required**<br>**Value type:** `Integer`<br>**Default value:** `10`
