# Create a new React component

## Simple CLI interface for creating React Functional Components

#### Forked from https://github.com/joshwcomeau/new-component.

# Install

## Globally for all projects

```bash
# Using Yarn:
$ yarn global add @gobzila/new-component

# or, using NPM
$ npm i -g @gobzila/new-component
```

## Locally for a specific project

```bash
# Using Yarn:
$ yarn add @gobzila/new-component

# or, using NPM
$ npm i @gobzila/new-component
```

# Quickstart
## Usage

```bash
$ cd PROJECT_DIRECTORY
$ new-component MyComponent
```

## What you'll get

In `src/components/MyComponent`:

```Javascript
// `MyComponent/MyComponent.js`
/**
 * Absolute imports
 */
import React from 'react';

/**
 * Import components and hooks
 */

/**
 * Other imports
 */

/**
 * Import props
 */
import { MyComponentProps, MyComponentDefaultProps } from './props';

const MyComponent = props => {
  return <></>;
};

MyComponent.propTypes = MyComponentProps;
MyComponent.defaultProps = MyComponentDefaultProps;

export default MyComponent;
```

```Javascript
// `MyComponent/props.js`
/**
 * Defines the data requirements for the component
 */
import PropTypes from 'prop-types';

/**
 * Defines the prop types
 */
const MyComponentPropTypes = {};

/**
 * Defines the default props
 */
const MyComponentDefaultProps = {};

export { MyComponentPropTypes, MyComponentDefaultProps };
```

```Javascript
// `MyComponent/index.js`
export { default } from './MyComponent';
export { MyComponentPropTypes, MyComponentDefaultProps } from './props';
```

## Configuration

### Directory

- Controls the desired directory for the created component. Defaults to `src/components`.
- Command line: `--dir <value>` or `-d <value>`.

### TypeScript

- Creates a React Functional Component for TypeScript project.
- Command line: `--type-script` or `-t`.
- What you'll get:

In `src/components/MyComponent`:

```TypeScript
// `MyComponent/MyComponent.js`
/**
 * Absolute imports
 */
import React from 'react';

/**
 * Import components and hooks
 */

/**
 * Other imports
 */

/**
 * Import props
 */
import { MyComponentProps, MyComponentDefaultProps } from './props';

const MyComponent: React.FC<MyComponentProps> = props => {
  return <></>;
};

MyComponent.defaultProps = MyComponentDefaultProps;

export default MyComponent;
```

```TypeScript
// `MyComponent/props.js`
/**
 * MyComponent props
 */
export interface MyComponentProps {}

/**
 * MyComponent default props
 */
export const MyComponentDefaultProps = {};
```

```TypeScript
// `MyComponent/index.js`
export { default } from './MyComponent';
export type { MyComponentProps } from './props';
export { MyComponentDefaultProps } from './props';
```