## Create a new React component

Forked from https://github.com/joshwcomeau/new-component.

### Install

#### Globally for all projects

```bash
# Using Yarn:
$ yarn global add @gobzila/new-component

# or, using NPM
$ npm i -g @gobzila/new-component
```

#### Locally for a specific project

```bash
# Using Yarn:
$ yarn add @gobzila/new-component

# or, using NPM
$ npm i @gobzila/new-component
```

### Usage

```bash
$ cd PROJECT_DIRECTORY
$ new-component TestComponent
```

### What you'll get

In `src/components/TestComponent`:

```Javascript
// `TestComponent/TestComponent.js`
/**
 * Absolute imports
 */
import React from 'react';

/**
 * Import other components and hooks
 */

/**
 * Import others
 */

/**
 * Import data
 */
import { propTypes, defaultProps } from './data';

/**
 * Displays the component
 */
const TestComponent = (props) => {
  return <></>;
};

TestComponent.propTypes = propTypes;
TestComponent.defaultProps = defaultProps;

export default TestComponent;
export {
  propTypes as TestComponentPropTypes,
  defaultProps as TestComponentDefaultProps,
};

```

```Javascript
// `TestComponent/data.js`
/**
 * Defines the data requirements for the component
 */
import PropTypes from 'prop-types';

/**
 * Defines the prop types
 */
const propTypes = {};

/**
 * Defines the default props
 */
const defaultProps = {};

export { propTypes, defaultProps };

```

```Javascript
// `TestComponent/index.js`
export {
  default,
  TestComponentPropTypes,
  TestComponentDefaultProps,
} from './TestComponent';

```