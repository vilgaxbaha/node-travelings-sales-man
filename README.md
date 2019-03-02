# node-travelings-sales-manInstallation
The openrouteservice client requires nodejs and a valid Api-Key to access the openrouteservice API. Also make sure that git is installed.

git
nodejs
Api-key
Permission Issues
If you encounter any permission issues during the installation:

on Linux: try running npm-commands with sudo :
e.g.:

sudo npm install
on Windows(GitBash recommended): try running npm-commands with the --no-optional flag:
e.g.:

npm install --no-optional
Step by Step instructions
Download openrouteservice repository:
# clone repository from github
git clone https://github.com/vilgaxbaha/node-travelings-sales-man

# switch to repository folder
cd openrouteservice-app
Install dependencies:
# install all modules listed as dependencies in package.json
npm install

# install dependencies listed in bower.json
node_modules/bower/bin/bower install
Install required modules for slider layout:
(This step is for layout purposes only. If you want to skip it remove grunt:sliderMakeCss from the task queue in the renamed Gruntfile.js [see next step])

# Switch to bower_components/angular folder:
cd bower_components/angularjs-slider

# install all modules listed as dependencies in package.json
npm install

# switch back to openrouteservice-app folder:
cd ../..
Initiate default files:
# Copy `Gruntfile.default.js` to `Gruntfile.js`
cp Gruntfile.default.js Gruntfile.js

# Copy `weathercheck.default.txt` to `weathercheck.txt`.
cp app/weathercheck.default.txt app/weathercheck.txt
Replace weathercheck.txt content with your Api-Key:
# Finally open `app/weathercheck.txt` in your favorite text editor and replace the content with your Token.
# e.g.:
vim app/weathercheck.txt
Run openrouteservice:
For the standard openrouteservice version do:

grunt ors
If you want to use the openrouteservice client with a local backend version of openrouteservice you have to adjust the endpoint paths to the backend war version you are using in Grunfile.js.

Afterwards do:

grunt ors_local
