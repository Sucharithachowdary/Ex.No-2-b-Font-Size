
# Ex.No:2 Develop an application that uses Font Size using Android Studio.


## AIM:
To develop an application that uses Font Size using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Create a New Android Project:
              • Click New in the toolbar.
              • In the window that appears, open the Android folder, select Android Application Project,
              and click next.
              • Provide the application name and the project name and then finally give the desired
              package name.
              • Choose a launcher icon for your application and then select Blank Activity and then click
              Next
              • Provide the desired Activity name for your project and then click Finish.

Step 2: Create a New AVD (Android Virtual Device):
        • click Android Virtual Device Manager from the toolbar.
        • In the Android Virtual Device Manager panel, click New.
        • Fill in the details for the AVD. Give it a name, a platform target, an SD card size, and
        a skin (HVGA is default).
        • Click Create AVD and Select the new AVD from the Android Virtual Device
        Manager and click Start.

Step 3: Design the graphical layout with a text view and two command buttons.

Step 4: Run the application.

Step 5:On pressing the change font size button, the size of the font gets altered.       
       
Step 6:Close the Android project. 


## Program:
 ```
/*
Program to Develop an application that uses Font Size using Android Studio .
Developed by: sucharitha 
RegisterNumber:  212221240021
*/
```

## MainActivity.java:

~~~

package com.firstapp.fontsize;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;

import android.app.Activity;
import android.graphics.Typeface;
import android.graphics.Color;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;


public class MainActivity extends AppCompatActivity {
    float font = 24;
    int i = 1;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t1 = (TextView)findViewById(R.id.textView1);
        Button b1 = (Button)findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener()    {
            public void onClick(View view) {
                t1.setTextSize(font);
                font = font+4;
                if(font==40)
                    font = 20;
            }
        });


    }
}
~~~



## activity_main.xml:
~~~
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <TextView
        android:id="@+id/textView1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="70dp"
        android:gravity="left"
        android:text="HELLO WORLD"
        android:textSize="20sp"
        android:textStyle="bold"
        tools:layout_editor_absoluteX="70dp"
        tools:layout_editor_absoluteY="376dp" />

    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20sp"
        android:gravity="center"
        android:text="Change Font Size"
        tools:layout_editor_absoluteX="40dp"
        tools:layout_editor_absoluteY="456dp" />
    </RelativeLayout>
~~~
## Output:
![233933812-a4ecd24d-3d3d-4ec5-ae8f-09526c2d4cfa](https://user-images.githubusercontent.com/94166007/233954079-70139c79-3f24-4dd8-b4b4-a6f29a8eeaf3.jpg)
![233933825-e970c3cf-88ef-44fb-9990-ec5417adeeb6](https://user-images.githubusercontent.com/94166007/233954089-69ed9aed-c9b2-4786-8e11-eb4f0e307696.png)



## Result:
Thus, the program for android application, Font Size was executed successfully using Android Studio.
