# Natours
Implemented as part of Udemy course to learn advanced features in CSS.

## Nodejs installation and SASS setup
1. Install nodejs from [here](https://nodejs.org/en/).

1. Confirm node is installed by typing *node -v* in the terminal.

1. Navigate into project folder using the terminal commands.

1. Create package.json file by typing *npm init* in the terminal.
    + This will prompt several questions for creating the file. In most cases the fields can be left blank or default values used.
    + If you download/clone someone's project and want to install all dependencies simply run *npm install* in the terminal and 
    all dependencies in the package.json file will be installed. This illustrates the main purpose of this file. Another scenario is working on one project on more than one computer.
    + When uploading a project to a repository don't upload the node_modules file as it is not necessary.

1. Install SASS npm package by typing *npm install node-sass --save-dev* in the terminal.
    + The --save-dev saves the development dependencie in the package.json file.
    + Other packages such as jQuery should be saved as *--save* because they are non-development dependencies.
    + To uninstall a package (jQuery example) type *npm uninstall jquery --save* in the terminal.

## Creating and compiling SASS/SCSS file
1. Create sass folder.
1. Create main.scss file.
1. Copy all content of style.css into it.
1. Modify package.json file
    ```javascript
        "scripts": {
            "compile:sass": "node-sass sass/main.scss css/style2.css -w"
        },
    ```
    + *compile:sass* is the name of the command we will use in the terminal.
    + *sass/main.scss* is the name and location of the SASS file to compile.
    + *css/style2.css* is the CSS file you want SASS to create and it's location.
    + *-w* is a watch command that will keep the compiler running in the terminal and update the CSS file every time the SASS file is saved.
1. Type *npm run compile:sass* in the terminal to compile the SASS file.

## Automatically reloading a page on file changes
1. Run *npm install live-server -g* to install live-server globally
    + The *-g* is for a global installation of the package so that it could be used on any project.
1. Run *live-server* to activate the package which will automatically open the html file.
    + This will run a local server and refresh the page every time a page edit and save occurs.
    + For this to work with the SASS compiler we need two terminals running, one for the SASS compiler watching and one for this package.


## Tools & Technologies

* HTML5
* CSS3
* npm
* live-server
* node-sass

## Acknowledgments

* Implemented as part of the online course on Advanced CSS by Jonas Schmedtmann
