# Getting Started with Create React App


*   Create new react App :: __`npx create-react-app <app-name>`__
    * It will create new react application with all the packages installed.
*   Add Storybook to React App :: __`npx sb init`__
    * This is will add extra package related to story book in to our react app.
    1. pacakage.json:
        *   This file will updates with the required installation of dependencies
            * In devDependencies & scripts below packages will get install
                ``` javascript
                 "devDependencies": {
                        "@storybook/addon-actions": "^6.1.10",
                        "@storybook/addon-essentials": "^6.1.10",
                        "@storybook/addon-links": "^6.1.10",
                        "@storybook/node-logger": "^6.1.10",
                        "@storybook/preset-create-react-app": "^3.1.5",
                        "@storybook/react": "^6.1.10"
                }
                "scripts": {
                    ----------
                    ----------
                    ----------
                    "storybook": "start-storybook -p 6006 -s public",
                    "build-storybook": "build-storybook -s public"
                }
                ```
    2.  .storybook (folder):
        *   At the top level with in the project folder `sb init` command will create this folder with two files
        *   main.js:
            *   Will export an object with two properties
            ``` javascript
            module.exports = {
                "stories": [ // This indicated all files in the src folder  that end with the extension stories.mdx and stories.js/jsx/ts/tsx are treated as stories for our story book app.
                    "../src/**/*.stories.mdx",
                    "../src/**/*.stories.@(js|jsx|ts|tsx)"
                ],
                "addons": [
                    "@storybook/addon-links",
                    "@storybook/addon-essentials",
                    "@storybook/preset-create-react-app"
                ]
            }

            ```
        *   preview.js:
            * It contains configuations for our stories we write.
    3.  src/stories (folder): It will create bolier plate code.
        *   `assets` (folder): This will have images and other files.
        *   `Introduction.stories.mdx`: this will be the landing page when running the story book.
        *   Along with this it will create 3 components:
            * Button component
            * Header component 
            * page component
            It for each component it will create .js where component is defined, .css file where the style are defined & .stories.js file contains the soried corresponding to the component.
*   Run the story book using the command __`npm run storybook`__




This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.\
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can’t go back!**

If you aren’t satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you’re on your own.

You don’t have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn’t feel obligated to use this feature. However we understand that this tool wouldn’t be useful if you couldn’t customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
