# Firefox Fixes

Firefox forms have some issues with dark gtk themes. For example, if webdevelopers set the font color to a dark color, but don't change the background of the form, it'll take the color for dark theme, making both the background and font color dark, which doesn't bode well.

## Work Around
- Find your firefox profile folder: http://kb.mozillazine.org/Profile_folder_-_Firefox#Finding_the_profile_folder
- Create a **chrome** folder if it doesn't exist
- Inside the chrome folder, create a **userContent.css** file
- Add this to your userContent.css file (modification of solution on ArchWiki https://wiki.archlinux.org/index.php/Firefox#Unreadable_input_fields_with_dark_GTK.2B_themes):

        input:not(.urlbar-input):not(.textbox-input):not(.form-control):not([type='checkbox']) {
            -moz-appearance: none !important;
            background-color: white !important;
            color: black !important;
        }

        #downloads-indicator-counter {
            color: white !important;
        }

        textarea {
            -moz-appearance: none !important;
            background-color: white !important;
            color: black !important;
        }

        select {
            -moz-appearance: none !important;
            background-color: white !important;
            color: black !important;
        }
