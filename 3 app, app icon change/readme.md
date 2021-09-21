### change icon of app

### got to url : appicon.co
<br>
<img width="450px" src= "icon generator.JPG"/> <br>
<br><br>
## stract the zip file 


<img width="" src= "place icon in project.JPG"/>
<img width="500px" src= "for android icon.JPG"/>

<img width="500px" src= "for ios icon.JPG"/>






##  code:
```
import 'package:flutter/material.dart';


void main() {

  runApp(

    MaterialApp //material class

        (

//poperty

      home: Scaffold(

        backgroundColor: Colors.white70, //back ground color poperty

        appBar: AppBar(

          title: Text('i am Rich'), //wigets

          backgroundColor: Colors.red,

          centerTitle: true,

        ),

        body: const Center(

          child: Image(

                  //image wegit

            image:

                  AssetImage('images/172780.jpg'),

         ),

        ),

      ),

    ),

  );

}

```


### to resize the icon in android: go to 'project' bar, android->app->src->main->res
### right clic on "res" = new -> image asset 

