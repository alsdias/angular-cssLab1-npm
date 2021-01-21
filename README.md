# angularx.cssLab1-npm Project 



## TARGET 



![](M:\work\devcli_\javascript\jstopics_bitbucket\cssLab1\support\img\angular_cssLab1.jpg)



## METHOD2 - USING NPM INSTALLER

**1. Install bootstrap using npm:**

- For Bootstrap 3:

  npm install bootstrap@3.3.7

- For Bootstrap 4:

  npm install bootstrap@4.5.3

- For latest Bootstrap version:
  npm install bootstrap



**2. Import the CSS.**

Two alternatives:



**2a. Edit "angular.json" and set:**

	"styles": [
	  "src/styles.css",
	  "node_modules/bootstrap/dist/css/bootstrap.css",
	  "src/styles/css/album.css"
	],



**2. If desired jquery, do:**
npm install jquery popper.js –save

Edit angular.json and set:

            "scripts": [
            	"node_modules/jquery/dist/jquery.js",
            	"node_modules/popper.js/dist/umd/popper.js",
            	"node_modules/bootstrap/dist/js/bootstrap.js"
            ]



## **OBSERVATION**

Personally, I do not use the "@import" annotation. Something like this:

*@import "../../../node_modules/bootstrap/dist/css/bootstrap.min.css";*

The configuration when is set on "angular.json" file is a much better option.




## ***\**IMPORTANT NOTE:**

Don't use the assets directory to set the CSS files.
When deploying to the production using Angular CLI, the CSS files registered in angular.json are minified and bundled into a single styles.css.
The assets folder is copied to the dist folder during the build process then, the CSS code get duplicated.
Only place CSS files under assets if importing them directly in the index.html.

 