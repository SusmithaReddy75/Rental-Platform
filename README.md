# Totality Frontend Challenge

## Project Overview
This project is a property rental platform developed using React. It features property listings, booking management, and a checkout process.

## Tech Stack
- React
- Redux (for state management)
- Material-UI (for UI components)
- Axios (for API calls)
- Formik and Yup (for form handling and validation)
- Stripe (for payment processing)
- Firebase (for authentication)

## Features
- Property Listings
- Booking Management
- Checkout Process
- Responsive Design
- User Authentication (optional)
- Property Reviews (optional)
- Favorites List (optional)
- ----------------------------------------------------------------------------------------------------------------------------------------------

## Running the Project Locally
1. Clone the repository:
   ```sh
   git clone https://github.com/your-username/totality-frontend-challenge.git


   # `react-is`

This package allows you to test arbitrary values and see if they're a particular React element type.

## Installation

```sh
# Yarn
yarn add react-is

# NPM
npm install react-is
```

## Usage

### Determining if a Component is Valid

```js
import React from "react";
import * as ReactIs from "react-is";

class ClassComponent extends React.Component {
  render() {
    return React.createElement("div");
  }
}

const FunctionComponent = () => React.createElement("div");

const ForwardRefComponent = React.forwardRef((props, ref) =>
  React.createElement(Component, { forwardedRef: ref, ...props })
);

const Context = React.createContext(false);

ReactIs.isValidElementType("div"); // true
ReactIs.isValidElementType(ClassComponent); // true
ReactIs.isValidElementType(FunctionComponent); // true
ReactIs.isValidElementType(ForwardRefComponent); // true
ReactIs.isValidElementType(Context.Provider); // true
ReactIs.isValidElementType(Context.Consumer); // true
ReactIs.isValidElementType(React.createFactory("div")); // true
```

### Determining an Element's Type

#### Context

```js
import React from "react";
import * as ReactIs from 'react-is';

const ThemeContext = React.createContext("blue");

ReactIs.isContextConsumer(<ThemeContext.Consumer />); // true
ReactIs.isContextProvider(<ThemeContext.Provider />); // true
ReactIs.typeOf(<ThemeContext.Provider />) === ReactIs.ContextProvider; // true
ReactIs.typeOf(<ThemeContext.Consumer />) === ReactIs.ContextConsumer; // true
```

#### Element

```js
import React from "react";
import * as ReactIs from 'react-is';

ReactIs.isElement(<div />); // true
ReactIs.typeOf(<div />) === ReactIs.Element; // true
```

#### Fragment

```js
import React from "react";
import * as ReactIs from 'react-is';

ReactIs.isFragment(<></>); // true
ReactIs.typeOf(<></>) === ReactIs.Fragment; // true
```

#### Portal

```js
import React from "react";
import ReactDOM from "react-dom";
import * as ReactIs from 'react-is';

const div = document.createElement("div");
const portal = ReactDOM.createPortal(<div />, div);

ReactIs.isPortal(portal); // true
ReactIs.typeOf(portal) === ReactIs.Portal; // true
```

#### StrictMode

```js
import React from "react";
import * as ReactIs from 'react-is';

ReactIs.isStrictMode(<React.StrictMode />); // true
ReactIs.typeOf(<React.StrictMode />) === ReactIs.StrictMode; // true
```

