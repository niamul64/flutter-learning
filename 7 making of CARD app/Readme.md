##i can use flutter inspector to inspect the app a screen and code structure 

### steps,

1. Make a directory in the project file called "images"
<br>
2. now goto the "pubspec.yaml"<br>
under the flutter:<br>
```
  assets:
    - images/ 
```
<br>
To grab all picture from images directory<br>
note: Always click on Pub get or packages get, after any change on "pubspec.yaml" file
<br>

3. now take a picture at the images directory(giving name "pic.jpg")
<br>
4. Now, in a StatelessWidget app of any name(i am giving an name 'MyApp')<br>
## return MaterialApp.

Materialapp-->Scaffold(AppBar, FloatingAcctionButton, body) -->(inside body) SafeArea--> Column--> childrean: CircleAvatar, Containers
<br>


### now inside children of column: 
[<br>
CircleAvatar: give radius, backgroundImage: AssetImage('images/pic.jpg'),<br>
<br>
Text:"Niamul Hasan", we can use style property <br>
(i can use control+q to see what i can use in Text widget)<br>
<br>
Container: child:--> Row--> children:<Widget>[   Icon()   ]

]




###using the different font in Text widget:
use Url: fonts.google.com
see video with this section.


### using of icon 
visit:--> <br> https://api.flutter.dev/flutter/material/Icons-class.html<br>
https://www.materialpalette.com/<br>
see video with this section