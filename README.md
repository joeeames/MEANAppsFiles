MEANAppsFiles
=============
This course is NOT up to date. Express 4.0 has been released, and this course uses 3.x. Because of this major portions of the course will not work if you follow along if you simply install the latest express. 

In order to work around this, if you just use express version 3, then everything will work. You can do this by changing the install command in Module 2 in the section "Creating the package.json file" to be:

npm install --save express@3.4.4 jade
instead of
npm install --save express jade

This will install version 3.4.4 of express.

The course will be updated approximately the end of May.

Notes:
To run the node server, type "node web-server.js" from the directory that contains the web-server.js file