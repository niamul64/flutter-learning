## see the video

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
          child: Icon(Icons.add),
        ),


        backgroundColor: Colors.teal,
        body: SafeArea(
          child: Column( /// same for Row Column
            children: <Widget>[
              Container(
                height: 100.0,
                width: 100,
                /// height width   END
                /// margine
                // margin: EdgeInsets.all(20), /// margine for all sides
                // margin: EdgeInsets.symmetric(vertical: 10, horizontal: 10),// top, bottom
                //margin: EdgeInsets.fromLTRB(30,60,10,10),// left, top, right, bottom,
                margin: EdgeInsets.only(left: 10, top:10),// only any of sides
                /// padding
                padding: EdgeInsets.all(10), /// padding is similar to margine
                /// padding        END
                color: Colors.white, // text color
                child: Text('con 1'),

              ),//1st
              Container(
                width: 100,height: 100,
                color: Colors.blueAccent,
                margin: EdgeInsets.only(left: 10, top:10),
                padding: EdgeInsets.all(10),
                child: Text('con 2'),
              ),//2nd
              Container(
                width: 100,height: 100,
                color: Colors.blueAccent,
                margin: EdgeInsets.only(left: 10, top:10),
                padding: EdgeInsets.all(10),
                child: Text('con 3'),
              ),//3nd
            ],

          ),



        ),

      ),
    );
  }
}


```