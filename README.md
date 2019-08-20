# OffCanMenu

Off-Canvas Menu to be used on any site

# Integration #

**Add bower.json dependency**

```
#!json

"off-can-menu":  "git@bitbucket.org:foremostmedia/offcanmenu.git#1.5.8"
```

**Add to application.scss**

```
#!scss
"../../bower_components/off-can-menu/assets/stylesheets/off-can-menu"
```

**Add to application.js** *(above project)*

```
#!js
//= require ../../bower_components/off-can-menu/assets/scripts/off-can-menu
```


**Add following to main.js with the selector being your wrapper to your menu**
```
$('nav.fmCleanMenu').offCanMenu();
```

## Options

```
menuLayout: {
    direction: 'right',
    closeMenu: true,
    login: true,
    menuLogo: '/Portals/_default/Skins/Offcan-Test/img/site-logo.png',
    animationBounce: '1.3',
    //buttonLocation: $('.site-footer'),
    buttonText: 'MENU',
    sideLinks: [
        { icon: 'fa fa-facebook-square', href: 'https://www.facebook.com/DNN-Awards-1826745947627503/' },
        { icon: 'fa fa-twitter-square', href: 'https://www.facebook.com/DNN-Awards-1826745947627503/' },
        { icon: 'fa fa-instagram', href: 'https://www.facebook.com/DNN-Awards-1826745947627503/' }
    ]
},
menuDimensions: {
    screenWidthTrigger: htmlHeight > windowHeight ? 1183 : 1200,
    menuWidth: 400,
    sideLinksWidth: 50,
    responsiveScreenWidthTrigger: 500,
    responsiveMenuPercent: 0.8
},
menuIcons: {
    closeIcon: '<i class="fa fa-close"></i>',
    backIcon: '<i class="fa fa-reply"></i>',
    navIcon: '<i class="fa fa-chevron-right"></i>',
    loginIcon: '<i class="fa fa-sign-in"></i>',
    logoutIcon: '<i class="fa fa-sign-out"></i>'
}
```

## Options Continued...

Name | Description | Options
------------- | ------------- | -------------
side | Sets side of screen menu will slide from | 'left','right'
closeMenu | Determines if a link to close the menu is inside top level of the menu | true,false
width | Sets threshold in pixels to enable menu on non-mobile devices | Number
MenuWidth | Base menu width - used when calculating smaller menu | Number
smMenuWinWidth | Sets threshold in pixels to shrink menu | Number
smMenuVar | Variable used to shrink menu | Number < 1
buttonLocation | Location of button injection | JQuery Selector 
buttonCode | Code to be rendered within button wrapper | HTML