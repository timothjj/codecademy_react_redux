# codecademy_react_dedux

## React

### Project 1: my-react-app

Create React projects Using Vite

1. Check version of node (must be v20+)
`node -v`

2. Update npm

`sudo npm install -g npm@latest`

3. Create React Project

`npm create vite@latest`

4. Follow prompts to 
- enter project name
- select React as the framework
- choose Javascript or Typescript

<em>Or combine options directly into the command line</em>
`npm create vite@latest my-react-app -- --template react`

This should result in the following output:
`found 0 vulnerabilities
│
◇  Starting dev server...

> my-react-app@0.0.0 dev
> vite


  VITE v7.3.0  ready in 275 ms

  ➜  Local:   http://localhost:5173/
  ➜  Network: use --host to expose
  ➜  press h + enter to show help`

        Vite has set up the following directories and files:

        Key Directories
        /node_modules

        This directory contains all the dependencies and sub-dependencies specified in your package.json file. You don’t need to modify anything here, and it’s automatically added to .gitignore since these files don’t need to be committed to your repository.

        /public

        This directory contains static assets that will be served directly without being processed by Vite. Files in this directory will be copied to the build directory during production. It contains:

        vite.svg - The Vite logo, which you can replace with your own favicon.
        /src

        This is where your React application code lives and where you’ll spend most of your time. The initial structure includes:

        /assets - a directory for storing static assets like images that will be processed by Vite
        App.jsx - the main React component of your application
        App.css - styles for the App component
        main.jsx - the entry point for your React application (this file serves the same purpose as index.js or index.jsx in other React setups)
        index.css - global styles for your application
        Note: Throughout Learn React, we’ll refer to index.jsx as the entry point file, which is common in many React projects. In Vite’s default template, this file is named main.jsx instead, but it serves the exact same purpose. If you prefer to follow the lessons exactly, you can rename main.jsx to index.jsx and update the script reference in index.html accordingly.

        Key Files
        index.html Located in the root directory, this HTML file serves as the entry point for your application. Vite injects your JavaScript into it during the build process. You can directly edit this file to add meta tags, change the page title, or include additional scripts or styles.

        package.json This file outlines all the settings for your React app, including:

        dependencies required for the application
        scripts for development, building, and previewing your app
        other metadata about your project
        Here, you’ll find important scripts like:

        dev: starts the development server
        build: creates a production-ready build
        preview: serves the production build locally for testing
        vite.config.js This is the configuration file for Vite, where you can customize the build tool’s behavior. By default, it simply includes the React plugin, but you can extend it to add features like:

        alias paths for imports
        custom build options
        additional plugins
        proxy settings for API requests
        eslint.config.js This file configures ESLint for your project, which helps catch errors and enforce code style. The Vite template comes with a basic configuration that extends the React recommended rules.

        .gitignore This file tells Git which files and directories to ignore when committing code, such as node_modules, build directories, and environment files.

        As your React app grows, it is common to add a /components directory to organize components and component-related files and a /views directory to organize React views and view-related files.

5. Open http://localhost:5173/ to see the current app interface

Any changes to the source code will live updated here. 

6. Work in App.jsx to make changes

There are currently two apps in the file. One is commented out. 

######################################################################

### Project 2: Authorization Form 

A client just called you to say that they love their new website! There’s only one problem: they don’t like how their contact page displays their personal information for all to see.

They’ve asked you to hide their website’s contact page behind a password form. In this project, you’ll accomplish this by creating a React component to set up a simple authorization layer.

