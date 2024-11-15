# Ex_02: Develop an application that uses GUI Components with Fonts and Colors

### DATE:

## AIM:
To develop an application that uses GUI Components with Fonts and Colors using android studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
1. Start a new Android project by selecting *New*> *Android Application Project*, provide the app and package name, choose a launcher icon, select *Blank Activity*, name the activity, and click *Finish*.

2. Open *Android Virtual Device Manager*, create a new AVD by providing its name, platform target, SD card size, and skin, then select and start the AVD.

3. Design the layout with a *TextView* and two buttons for changing font size and color.

4. Run the application to test it.

5. Use the *Change Font Size* button to adjust text size and the *Color* button to change text color, then close the project.


## Program:
 ```
/*
Program to Develop an application that uses Font Size using Android Studio .
Developed by:  Priya R
RegisterNumber:  212222040124
*/
```

## MainActivity.java:

```
package com.example.myapplication;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.graphics.Color;
import android.widget.Button;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    int ch=1;
    float font=30;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= findViewById(R.id.textView);
        Button b1= findViewById(R.id.button1);
        b1.setOnClickListener(v -> {
            t.setTextSize(font);
            font = font + 5;
            if (font == 50)
                font = 30;
        });
        Button b2= findViewById(R.id.button2);
        b2.setOnClickListener(v -> {
            switch (ch) {
                case 1:
                    t.setTextColor(Color.RED);
                    break;
                case 2:
                    t.setTextColor(Color.GREEN);
                    break;
                case 3:
                    t.setTextColor(Color.BLUE);
                    break;
                case 4:
                    t.setTextColor(Color.CYAN);
                    break;
                case 5:
                    t.setTextColor(Color.YELLOW);
                    break;
                case 6:
                    t.setTextColor(Color.MAGENTA);
                    break;
            }
            ch++;
            if (ch == 7)
                ch = 1;
        });


    }
}

```




## activity_main.xml:

```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="center"
        android:text="Hello World!"
        android:textSize="25sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20dp"
        android:gravity="center"
        android:text="@string/change_font_size"
        android:textSize="25sp" />
    <Button
        android:id="@+id/button2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20dp"
        android:gravity="center"
        android:text="@string/change_color"
        android:textSize="25sp" />
</LinearLayout>

```

## Output:

![image](https://github.com/user-attachments/assets/8e7ac7c9-2b0f-4009-80d8-fa56e716e3b4)

![image](https://github.com/user-attachments/assets/af44ae2b-0608-452c-a588-05201901ab8e)






## Result:
Thus, the program for android application, Font Size and color was executed successfully using Android Studio.
