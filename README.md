# React Use HubSpot Form Embed

[![npm (scoped)](https://img.shields.io/npm/v/@groverj324/react-hubspot-form?style=flat-square)](https://www.npmjs.com/package/@groverj324/react-hubspot-form)
[![Bundle Size](https://img.shields.io/bundlephobia/min/@groverj324/react-hubspot-form?style=flat-square)](https://bundlephobia.com/result?p=@groverj324/react-hubspot-form)
![License](https://img.shields.io/npm/l/@groverj324/react-hubspot-form?style=flat-square)

Embed HubSpot forms into your React components using hooks! Works with Create React App, Gatsby and other platforms.

## Install

```
$ npm install --save @groverj324/react-hubspot-form
```

```
$ yarn add @groverj324/react-hubspot-form
```

## Getting Started

Wrap your application with `HubspotProvider`. This will add [Hubspot script](https://js.hsforms.net/forms/v2.js) to the head of your document.

```TypeScript
import React from 'react';

import { HubspotProvider } from '@groverj324/react-hubspot-form';

const MyApp = () => (
    <HubspotProvider>
        <MyPage />
    </HubspotProvider>
)

```

## Usage

```TypeScript
import React from 'react';

import { useHubspotForm } from '@groverj324/react-hubspot-form';

const MyPage = () => {
    const { loaded, error, formCreated } = useHubspotForm({
        portalId: 'XXXXXXX',
        formId: 'XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX',
        target: '#my-hubspot-form'
    });

    return (
        <div>
            <h1>Embed Form Below</h1>
            <div id="my-hubspot-form"></div>
        </div>
    )
}

```

## Breaking Changes

### 1.0.0

- Introduction of the `HubspotProvider` component. This needs to be included in your App for `useHubspotForm` to work.

## Support

If you feel like sending some sats to aaron@zbd.gg my [Lightning Address](https://zbd.gg/aaron/) it would be much appreciated.
