# Setting up a Webpack Project

## I. Setup Webpack

1. Run `npm init` in the project directory to generate a `package.json` file.

2. Run `npm install webpack webpack-cli --save-dev` to install webpack to the `node_modules` directory of your project.

3. Add a `.gitignore` file to ignore the `node_modules` folder when backing up to GitHub. Run `npm install` when downloading a project to install all dependencies.

4. Create a `src` directory with a `index.js` file.

5. Create a `dist` directory with `index.html` and `style.css` files.

6. Create a `webpack.config.js` file in the root of the folder.

## II. Link Your Files

1. Add text per files in this folder to `index.html`, `style.css`, and `webpack.config.js`.

2. Run `npx webpack --config webpack.config.js` to run the build; this should create the `main.js` file in the `dist` folder.

3. Run `npx webpack --watch` so you do not have to rerun webpack everytime you make a change.

## III. Add Testing Support

1.  In `package.json`, change the `test` line to read `"test": "jest"`.

2.  In order for jest to support ECMAScript, install Babel dependencies:

        npm install --save-dev babel-jest @babel/core @babel/preset-env

3.  Then, create a `babel.config.js` file in the root of your project with the following content:

        module.exports = {
            presets: [['@babel/preset-env', {targets: {node: 'current'}}]],
        };

4.  In your regular `example.js` file, export your functions to test as an object:

        module.exports = {
            add,
            subtract,
            multiply,
            divide
        }

5.  In your `example.test.js` files, a basic test looks like the following:

        const funcs = require('./example');

        describe("addative functions", () => {

            test('adds numbers correctly', () => {
                expect(funcs.add(10, 20)).toBe(30);
            })

            test('subtracts numbers correctly', () => {
                expect(funcs.subtract(10, 20)).toBe(-10);
            })
        })
