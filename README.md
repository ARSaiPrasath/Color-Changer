# Color-Changer
This is a chrome extension which changes the color of a tab in a chrome window.
Description:
So, in this project I have made a chrome extension where we can change the color of a tab by entering the color or by entering its respective color code. With the use of this extension we can easily change the color without installing any application to change it. So, I thought it would be a good idea to create a chrome extension which helps to change the color in a tab.

The project contains a pop-up form in which we should enter the color or its color code to change the color of the tab and then there is a “Change Color” button to enter and it changes the color of the tab. This is very easy and convenient to use. It will be helpful if we have to change color instantly. 

So, the project folder contains four files named ‘manifest.json’, ‘popup.html’, ‘popup.js’ and ‘content.js’.


Browsers usually parse web pages based on the json file specifically named manifest. This is the main configuration file of the chrome extension in which we have the important information related to the extension such as name, version and all other important things. This is a mandatory file to create when publishing the extension to the chrome store.  So, now we move on to my manifest.json file
The manifest.json file contains all the data and contains all the manifest details for any browser. It contains the version number ‘1.0’ for my chrome extension. It also contains browser action in which we add the default title of the form which is “Change Color” and the default pop-up and the icon for my chrome extension. And then, we add the image for the chrome extension.

The HTML files generally contain the skeletal figure for the extension. The HTML file is a normal HTML file, but the browser when reading it as an extension then parses it into a mini version of the same with the same functionality, just smaller and suitable for an extension. So now, we move on to my HTML code.
Popup.html file contains the base skeletal code for the extension.  In this file you will write your html code and take the user input, in which we have to enter the color or the color code and then pass this data to the Content Script and Background Script Using Chrome API. We finally add the script tag and reference the file in this tag at the end of the HTML file. This links the script to our JavaScript file, which is ‘script.js’ file.
The JS Script is put at the end of the file because it doesn’t have to load before the other contents of the extension / webpage.
Script.js file contains the working functionality of the extension. When the user clicks the button we are attaching the event listener and then we are getting the user input, that is, the color entered by the user and then we are passing this color to the content.js file.
After that, we create a new file in the same directory called as content.js, in which we get the color from popup.js and then it changes the color of the tab.
