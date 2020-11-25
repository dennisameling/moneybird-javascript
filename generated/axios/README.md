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
import { ContactsApi } from 'moneybird-axios';

const contactsApi = new ContactsApi({
    accessToken: 'YOUR_TOKEN',
    basePath: 'https://moneybird.com/api/v2/{ADMINISTRATION_ID}'
});

contactsApi.getContacts().then(response => {
    const contacts = response.data;
    for (let contact of contacts) {
        console.log(`Found contact: ${contact.firstname} ${contact.lastname}, ID ${contact.id}`);
    }
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
