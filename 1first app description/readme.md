import 'package:flutter/material.dart';<br>
<br>
void main() {<br>
  runApp(<br>
    MaterialApp //material class<br>
        (<br>
      //poperty<br>
      home: Scaffold(<br>
        backgroundColor: Colors.white70, //back ground color poperty<br>
        appBar: AppBar(<br>
          title: Text('i am Rich'), //wigets<br>
          backgroundColor: Colors.red,<br>
          centerTitle: true,<br>
        ),<br>
        body: Center(<br>
          child: Image(<br>
            //image wegit<br>
            image: NetworkImage(<br>
                'https://image.shutterstock.com/image-photo/northern-lights-above-reykjavik-iceland-260nw-176694704.jpg'),<br>
          ),<br>
        ),<br>
      ),<br>
    ),<br>
  );<br>
}<br>
<br>

<img width="" src= "i am rich app.JPG"/>


<img width="" src= "wigte tree.JPG"/>
<img width="" src= "scaffold.JPG"/>