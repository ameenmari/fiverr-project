# AIA Voting V2
## First Time Setup
1. Run `npm install` on the root directory
2. Rename `src/_config-sample.json` to `src/config.json`
3. In your new `config.json` set the `apiEndpoint` property.

## Configuration
1. To deploy the application to a subdirectory, change the `baseName` property to the subdirectory path
2. Set the root container where the app will be displayed by setting the `rootContainer` property

## Deploying to WordPress
1. Clone or switch to wp-setup branch
2. Open your config.json and replace the value of appPath constant to the slug of your WordPress page where the app will live.
3. Push the change and ssh into the server using the following credentials:
    - ssh -p 2200 aiaawards@170.249.212.110
    - Password: dRnPZ.KT56FD
4. Navigate to the app folder with the following command:
    - cd public_html/aia-nominations
5. Run git fetch --all && git checkout --force "origin/wp-setup"
6. Run "npm run build" command
7. Edit your wordpress page and place the following shortcode where it's needed [aia_nominations_app]. This shortcode will scan the build/static/js and build/static/css folders, and it will load all your css and js chunks. It will only load the css and js files if the shortcode is present on a page. The other pages won't have it.

## Available REACT Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
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

This section has moved here: https://facebook.github.io/create-react-app/docs/code-splitting

### Analyzing the Bundle Size

This section has moved here: https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size

### Making a Progressive Web App

This section has moved here: https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app

### Advanced Configuration

This section has moved here: https://facebook.github.io/create-react-app/docs/advanced-configuration

### Deployment

This section has moved here: https://facebook.github.io/create-react-app/docs/deployment

### `npm run build` fails to minify

This section has moved here: https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify
