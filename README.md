vibou.gTile
===========

Gnome-shell extension that tiles windows as you like.

This extension is developed at [GitHub](https://extensions.gnome.org/extension/28/gtile/)
If you are reading this documentation anywhere else, it might be out of date.

See also
--------

-   [vibou.gtile2](https://github.com/vibou/vibou.gTile2) - gnome shell extension that tiles windows as you like. With gSettings Support

Configration
------------

To configure gTile open the file extension.js
go down to SETTINGS comments
and edit this part of the code:

    /*INIT SETTINGS HERE TO ADD OR REMOVE SETTINGS BUTTON*/
    /*new GridSettingsButton(LABEL, NBCOL, NBROW) */
    function initSettings()
    {
        //Here is where you add new grid size button
        gridSettings[SETTINGS_GRID_SIZE] = [
            new GridSettingsButton('2x2',2,2),
            new GridSettingsButton('4x4',4,4),
            new GridSettingsButton('6x6',6,6)
        ];
        
        //example for new GridSettingsButton:
        myCustomButton = new GridSettingsButton('Custom',8,8); //Going to be a 8x8 GridSettings
        gridSettings[SETTINGS_GRID_SIZE].push(myCustomButton);
        
        
        /*NEW SETTINGS*/    
         //You can change those settings to set whatever you want by default
         //Afterward you can change those parameters using the gTile interface
         gridSettings[SETTINGS_AUTO_CLOSE] = true;
         gridSettings[SETTINGS_ANIMATION] = true;
    }

Author
------

This extension has been developed by [vibou](https://github.com/vibou) with the
help of the gnome-shell community. See
[network](https://github.com/vibou/vibou.gTile/network) for details.
           
CHANGE LOG
----------

### V12

-   Correct small bug on auto tile where monitor height was considered without gnome-panel on primaryMonitor

### V11

-   AutoTile function : 2 new auto tile features + Replace Animation and auto close text by icons
    
### V10
 
-   Now gTile follows your focus window !! Thanks to Claus Beerta he implements it in a branch.
-   I change the implementation so that it works with  multi-screen and I also added animations.
    
### V9

-   Not validated

-   However he added the keybinding in settings (into the file extension.js) but it s still buggy I think
-   So I let it for those who wants to try it.

### V8

-   Correct bug where Desktop can be tile
-   3x2 button added by default

### V7

-   Add Auto-close once resize
-   Add Smooth animation when toggle extension
-   New icon  
    (/!\ auto-close may cause some bugs so let me know if you had any thanks).

