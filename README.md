
Cordova Print Plugin - Example
==============================

[Cordova][cordova] plugin to print HTML documents using [AirPrint][AirPrint] and [Android Printing Framework][APF].

## Instructions
[Download][zip] the _example_ branch and run the following command.

```bash
cordova emulate [ios|android]
```

These will lunch the simulator or any plugged in device and start the example application as seen below in the screenshots. 

A click on the _PRINT SOME STUFF_ link opens the native print dialog to print out an HTML snippet.

```javascript
page = '';

page += '<h1>This is a main header<h1>';
page += '<h2>Thats a sub category</h2>';

cordova.plugins.printer.print(page, { landscape:false }, function () {
    alert('done');
});
```

Please read the plugin's [README][readme] for further requirements and informations.


### Testing in the iOS Simulator
There's no need to waste lots of paper when testing - if you're using the iOS simulator, select _File -> Open Printer Simulator_ to open some dummy printers (print outs will appear as PDF files).


### Testing in the Android Simulator
There's no need to waste lots of paper when testing - if you're using the Android simulator, select _Save to PDF_.

Dont forget to install a PDF viewer like [MuPDF][mupdf], otherwise Android will not open the file. Note that you need to install the app for the right hardware architecture!


## Screenshots iOS
![ios][ios_screens]


## Screenshots Android
![android][android_screens]


[cordova]: https://cordova.apache.org
[APF]: http://www.techotopia.com/index.php/Printing_with_the_Android_Printing_Framework
[AirPrint]: http://support.apple.com/kb/ht4356
[android_screens]: images/android.tiff
[ios_screens]: images/ios.tiff
[readme]: https://github.com/katzer/cordova-plugin-printer/blob/master/README.md
[zip]: https://github.com/katzer/cordova-plugin-printer/archive/master.zip
[mupdf]: http://www.mupdf.com