# Firefox Fixes

Firefox forms have some issues with gtk themes. It'll take the dark theme, for the background of the forms but then use black text font color, which doesn't bode well.

## Work Around
- Find your firefox profile folder: http://kb.mozillazine.org/Profile_folder_-_Firefox#Finding_the_profile_folder
- Create a **chrome** folder if it doesn't exist
- Inside the chrome folder, create a **userContent.css** file
- Add this to your userContent.css file:

        /**
        * Default colors for HTML-Forms when using dark GTK Themes.
        *
        * @author Julius Beckmann kontakt@juliusbeckmann.de
        */

        button,
        input,
        input[type="radio"],
        input[type="checkbox"],
        input[type="reset"],
        input[type="button"],
        input[type="submit"],
        select,
        textarea {
            -moz-appearance: none !important;
            background-color: white;
            color: black;
        }

