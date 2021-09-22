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
Container: child:--> Row--> children:<Widget>[   Icon() , Text()  ]

]


###using the different font in Text widget:<br>
use Url: fonts.google.com<br>
see video with this section.<br>


### using of icon 
visit:--> <br> https://api.flutter.dev/flutter/material/Icons-class.html<br>
https://www.materialpalette.com/<br>
see video with this section<br>

<br>
code:<br>
```
import 'package:flutter/material.dart';

void main() {
  runApp(MyApp());
}

class MyApp extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      home: Scaffold(

        appBar: AppBar(/// 1st element
          title: Text('i am Rich'), //wigets
          backgroundColor: Colors.red,
          centerTitle: true,
        ),

        floatingActionButton: FloatingActionButton(/// Floating element
          backgroundColor: Colors.red,
          child: Icon(Icons.home),
        ),


        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column (/// same for Row Column
            children: <Widget>[
              CircleAvatar(

                backgroundImage: AssetImage('images/pic.jpg'),
                radius: 70,
              ),
              Text(
                'Niamul Hasan',
                style: TextStyle(
                  fontSize: 30,
                  fontFamily: 'Bonheur',
                  color: Colors.white,
                  letterSpacing: 4,
                  fontWeight: FontWeight.bold,
                ),


              ),
              Text(
                'Flutter Developer',
                style: TextStyle(
                  fontSize: 25,
                  letterSpacing: 2,
                  color: Colors.white70,
                  fontWeight: FontWeight.bold,
                ),
              ),
              SizedBox(
                height: 10,
              ),
              Container(
                color: Colors.white,
                margin: EdgeInsets.fromLTRB(20,20,20,0),//left, top, right, bottom
                padding: EdgeInsets.all(5),
                child: Row(

                  children: <Widget>[


                    Icon(
                        Icons.phone,
                      size: 35,
                      color: Colors.teal,

                    ),
                    SizedBox(
                      width: 15,
                    ),
                    Text(
                        '+88017041...',
                      style: TextStyle(
                          color:Colors.black,
                        fontSize: 17,
                      ),

                    ),


                  ],
                ),
              ),

              Container(
                color: Colors.white,
                margin: EdgeInsets.fromLTRB(20,10, 20, 0),//left, top, right, bottom

                padding: EdgeInsets.all(5),
                child: Row(

                  children: <Widget>[
                    Icon(
                      Icons.email,
                      size: 35,
                      color: Colors.teal,

                    ),
                    SizedBox(
                      width: 15,
                    ),
                    Text(
                      'niamul@gmail.com',
                      style: TextStyle(
                        color:Colors.black,
                        fontSize: 17,
                      ),

                    ),


                  ],
                ),
              ),

            ],

          ),

        ),

      ),
    );
  }
}


```