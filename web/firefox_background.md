##
### How to customize firefox browser background:
##
Open firefox and in the address bar, type:
```
about:support
```
##
Find the `Profile Directory` and click on `Open Directory` to access your Firefox profile directory. 
##
Inside the profile directory, create a folder named `chrome` if it doesn’t already exist.
##
Inside the chrome folder, create a new directory called `img` and a file named: 
```
userContent.css
```
##
Move your desired `image` into the `img directory`.
##
Open userContent.css with a text editor and paste the following code, replacing `your-image.jpg` with the name of your image file:
```
@-moz-document url(about:home), url(about:newtab), url(about:privatebrowsing) {
  body::before {
    content: "";
    z-index: -1;
    position: fixed;
    top: 0;
    left: 0;
    background: no-repeat url(img/`your-image.jpg`) center;
    background-size: cover;
    width: 100vw;
    height: 100vh;
  }
}
```
##
Save the `userContent.css` file and close the editor.
##
In firefox address bar, search for:
```
about:config
```
Then search for:
```
toolkit.legacyUserProfileCustomizations.stylesheets
```
##
Toggle the value from `false` to `true`
##
Restart Firefox to see your custom image as the background.
##