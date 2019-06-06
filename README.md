# MobileStatusBarTheme
Simple Meta Tag solution for changing color theme of the Mobile Status Bar / Toolbar in Chrome, Firefox OS and Opera.

Insert these Meta tags in the <head> section of your HTML document and use only Hexadecimal as color Codes. 

<!-- Android -->
<meta name="theme-color" content="#ff6800">

<!-- Windows Phone -->
<meta name="msapplication-navbutton-color" content="#ff6800">

<!-- iOS / Safari  -->
<meta name="apple-mobile-web-app-capable" content="yes">
<meta name="apple-mobile-web-app-status-bar-style" content="black-translucent">

On iOS / Safari you can only change the appearance of the default status bar to either black or black-translucent. With black-translucent, the status bar floats on top of the full screen content, rather than pushing it down. This gives the layout more height, but obstructs the top. But first set the apple-mobile-web-app-capable meta tag to yes to turn on standalone mode.
