# MobileStatusBarTheme
Simple Meta Tag solution for changing color theme of the Mobile Status Bar / Toolbar in Chrome, Firefox OS and Opera.

Insert these Meta tags in the <head> section of your HTML document but use only Hexadecimal as color codes: 
```
<!-- Android -->
<meta name="theme-color" content="#ff6800">

<!-- Windows Phone -->
<meta name="msapplication-navbutton-color" content="#">

<!-- iOS / Safari  -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">
```
On iOS / Safari you can only change the appearance of the default status bar to either black or black-translucent. With black-translucent, the status bar floats on top of the full screen content, rather than pushing it down. This gives the layout more height, but obstructs the top. But first set the apple-mobile-web-app-capable meta tag to yes to turn on standalone mode.


Prefix and trick for older browsers in CSS:
```
#urlbar[level="high"] .autocomplete-textbox-container { background-color: #ff6800 !important; }
#urlbar[level="low"] .autocomplete-textbox-container { background-color: #ff6800 !important; }
#urlbar[level="broken"] .autocomplete-textbox-container { background-color: #ff6800 !important; }

@-moz-document url-prefix(chrome://browser/content/browser.xul) {
    #PopupAutoCompleteRichResult .autocomplete-richlistitem .ac-url-text,
    #PopupAutoCompleteRichResult .autocomplete-richlistitem .ac-separator-text,
    #PopupAutoCompleteRichResult .autocomplete-richlistitem .ac-action-text,
    #downloadsHistory { background-color: #ff6800 !important; }
} 
```
