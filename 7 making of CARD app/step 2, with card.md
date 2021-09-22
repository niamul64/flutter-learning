### card don't have a 'padding' element.
   

make the columun   centerd: SafeArea--> child: Column--> 
```
   /// making centered
            mainAxisAlignment: MainAxisAlignment.center,
   /// making centered END
```
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

Materialapp-->Scaffold(AppBar, FloatingAcctionButton, body) -->(inside body) SafeArea--> Column--> childrean: CircleAvatar, card, card
<br>


### now inside children of column: 
[<br>
CircleAvatar: give radius, backgroundImage: AssetImage('images/pic.jpg'),<br>
<br>
Text:"Niamul Hasan", we can use style property <br>
(i can use control+q to see what i can use in Text widget)<br>
<br>
card: child:--> ListTile(   Icon() , Text()  )

]




### code:

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
            /// making centered
            mainAxisAlignment: MainAxisAlignment.center,
            /// making centered END
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
                height: 20,
                width: 250,
                child: Divider(
                  thickness: 2, // thickness of the line
                  indent: 20, // empty space to the leading edge of divider.
                  endIndent: 20, // empty space to the trailing edge of the divider.
                  color: Colors.tealAccent, // The color to use when painting the line.
                  height: 20,
                ),
              ),

              Card(
                color: Colors.white,
                margin: EdgeInsets.fromLTRB(15,20,15,0),//left, top, right, bottom
                child: ListTile(
                  leading:  Icon(
                    Icons.phone,
                    size: 35,
                    color: Colors.teal,

                  ),
                  title: Text(
                      '+8801704159..',
                      style: TextStyle(
                        color:Colors.black,
                        fontSize: 17,
                      ),
                  ),
                ),

              ),

              Card(
                color: Colors.white,
                margin: EdgeInsets.fromLTRB(15,10, 15, 0),//left, top, right, bottom
                child: ListTile(
                  leading: Icon(
                    Icons.email,
                    size: 35,
                    color: Colors.teal,

                  ),
                  title:Text(
                    'niamul@gmail.com',
                    style: TextStyle(
                      color:Colors.black,
                      fontSize: 17,
                    ),

                  ) ,
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
