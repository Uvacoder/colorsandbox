![scenario](https://user-images.githubusercontent.com/132332/52920033-968ba580-3308-11e9-8230-24fe21e3a491.png)

A toolkit to clevery abstract, manage, document, export and preview your color palettes

## Features

* Define a simple ColorPalette
* Preview your programatically abstracted colors and rules
* See how colors would harmonize together inside your palette behaves
* Check which typography will work in which combination
* (WIP) Access the color abstraction methods via an easy API
* (WIP) Export all posible abstractions to CSS, Sketch, Photoshop, etc
* (WIP) Customize the abstraction rules
* (WIP) Enable multiple palettes
* (WIP) Embed your colors/abstraction combination into your website/document/etc

## Try it

[![scenario](https://user-images.githubusercontent.com/132332/53442167-ef45f700-3a08-11e9-99a3-9c866bc722d3.png)](https://scenario.netlify.com)

https://scenario.netlify.com


## How to use it

`yarn add @fivenp/scenario`

### (WIP) Color preview / documentation

```
import { Scenario } from '@fivenp/scenario'

class App extends React.Component {
  const myPalette = {
      'red' : '#ff0000',
      'green' : '#00ff00',
      'blue' : '#0000ff',
      'yellow' : '#ffff00',
  }

  public render(): JSX.Element {
    return (
      <Scenario colors={myPalette} />
    )
  }
}

export default App
```

### (WIP) Helper functions API

```
import { lighten } from '@fivenp/scenario'

const red = '#ff0000'
const myLightRed = lighten(red)

```

## (WIP) Props & Helper functions

Scenario consists of two parts - one for previewing/documenting your colors - and one providing you with the matching rules for the abstractions.

### (WIP) Props for `<Scenario />`

| prop             | type       | default    | required   | description
| ---------------- | ---------- | ---------- | ---------- | ----------
| colors           | *object*   | `N/A`      | **yes**    | The palette object defining you color palette

### (WIP) Exposed helper functions

#### lighten(color)

Lightens the provided HEX color. It programatically converts it to HSL, removes 10% of Saturation and adds 10% of Lightness to it. Returns a valid hex color

| argument         | type       | description
| ---------------- | ---------- | ----------
| color            | *string*   | Must be a valid *hex* color - e.g. #ff0000


#### darken(color)

Darkens the provided HEX color. It programatically converts it to HSL, adds 10% of Saturation and removes 10% of Lightness to it. Returns a valid hex color

| argument         | type       | description
| ---------------- | ---------- | ----------
| color            | *string*   | Must be a valid *hex* color - e.g. #ff0000

## Local development

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

You can find information about how to set up a local devenv over [here](https://github.com/fivenp/scenario/blob/master/CONTRIBUTING.md#setting-up-the-project-locally)

### Available Scripts

In the project directory, you can run:

#### `yarn start`

Runs the app in the development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will also see any lint errors in the console.

#### `yarn test`

Launches the test runner in the interactive watch mode.<br>
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

#### `yarn run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

#### `yarn run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (Webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Useful resources
