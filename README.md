<h1 align="center">
  webtrader-charts
</h1>

The charting library extracted from [Webtrader](https://github.com/binary-com/webtrader) is used for binary-static and webtrader.

![Build Status](https://travis-ci.org/binary-com/webtrader-charts.svg?branch=master)

## In this document:

-   [Other Documents](#other-documents)
-   [Pre-installation](#pre-installation)
-   [Quick start](#quick-start)
-   [How to contribute](#how-to-contribute)
-   [Manage translations](#manage-translations)
-   [Deploying to gh-pages](#deploying-to-gh-pages)
-   [Publishing to npm](#publishing-to-npm)

## Other Documents

-   [General implementation](documents/implementation-guide.md) - Contain ways to use the library

## Pre-installation

Before running or contribute to this project, you need to have the setup of the following packages in your environment

-   node 
-   npm
-   git 

## Quick start

1.  **Fork the project**

    In order to work on your own version, please fork the project to your own repo.

2.  **Clone using SSH**

    ```sh
    git clone git@github.com:your-github-username/webtrader-charts.git
    ```

3.  **Enter project directory**

    ```sh
    cd webtrader-charts
    ```

4.  **Change output folder:**

   - Change `rollup.config.js` to write the output into `/example` folder.

    **NOTE: you can change the `dist` file config in `rollup.config.js` by uncommenting the file prop for `example`, `webtrader` or `binary-static`

5.  **Install your dependencies:**

   - run the following command on both main project and `/example` folder:

    ```sh
    yarn install
    ```

6.  **Start developing:**

   - run the following command on both main project and `/example` folder:

    ```sh
    yarn watch
    ```

7.  **Open the source code and start editing!**

    Your site is now running at `http://localhost:8000`!


## How to contribute

1. Create branch from the latest dev branch

    ```sh
    git checkout dev
    git pull upstream dev
    git checkout -b [_your_branch_name]
    ```

2. Make your changes

3. Make pull request

-   Push your changes to your origin

    ```sh
    git push -u origin [_your_branch_name]
    ```

-   Click on the autogenerated link from the terminal to open the PR

-   Make sure to change the PR base to `dev` branch

## Manage translations

- to get the `dictionary.json` file:

   ```sh
   yarn build-translation
   ```

- The language files `/src/i18/{lang}.json` files.
- The library uses the generated `dictionary.json` file.

## Deploying to gh-pages

- To deploy the `/example` folder:
   
   ```sh
   yarn deploy-example
   ```

- To deploy latest version embedded in binary-static (for testing)

   ```sh
   yarn deploy-hard
   ```

   **NOTE: For the second time you are deploying, run the following command:

   ```sh
   yarn deploy-soft
   ```

## Publishing to npm

1. Run:

   ```sh
   yarn install
   ```

2. Update the files `dist/webtrader-charts.js` and `dist/webtrader-charts.iife.js`

   ```sh 
   yarn run build
   ```

3. Update the package version in package.json

4. Commit the modified files and merge them into the repo

5. Run: 

   ```sh 
   npm publish
   ```

