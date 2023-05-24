# moneybird-axios

This package provides a TypeScript/JavaScript client for the Moneybird API and utilizes [axios](https://github.com/axios/axios).

It can be used in both TypeScript and JavaScript. In TypeScript, you can benefit from things like type hints.

## Installation

Navigate to the folder of your consuming project and run the following command to install the package:

```shell
npm install moneybird-axios --save
```

## Usage

```TypeScript
import { AdministrationsApi, Configuration } from 'moneybird-axios';

const administrationsApi = new AdministrationsApi(<Configuration>{
    accessToken: 'YOUR_TOKEN'
});

administrationsApi.getAdministrations().then(response => {
    const administrations = response.data;
    administrations.forEach(administration => {
        console.log(`Found administration: ${administration.name}`);
    });
}).catch(e => {
    console.error(`Error: ${e}`);
});
```

### Building

To build and compile the TypeScript sources to JavaScript, use:

```shell
npm install
npm run build
```
