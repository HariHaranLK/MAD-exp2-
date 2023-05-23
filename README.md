# Ex.No:1 To create a HelloWorld Activity using all lifecycles methods to display messages.


## AIM:

To create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “Hello World”.
Developed by: Hari Haran L K
Registeration Number :212221040051
*/
```
**XML FILE:**
    
    
    <?xml version="1.0" encoding="utf-8"?>
    <androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
      xmlns:app="http://schemas.android.com/apk/res-auto"
      xmlns:tools="http://schemas.android.com/tools"
      android:layout_width="match_parent"
      android:layout_height="match_parent"
      tools:context=".MainActivity">

    <Button
        android:id="@+id/colbut"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="128dp"
        android:layout_marginTop="120dp"
        android:backgroundTint="#FFC107"
        android:text="Change Color"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/fonbut"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="132dp"
        android:layout_marginTop="48dp"
        android:backgroundTint="#FF5722"
        android:text="Change Font"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/colbut" />

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_marginStart="48dp"
        android:layout_marginTop="152dp"
        android:text="PRIME PLAYS"
        android:textSize="40dp"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/fonbut" />
    </androidx.constraintlayout.widget.ConstraintLayout>
        
**MAINACTIVITY:**
    
    package com.example.guicomps;

    import androidx.appcompat.app.AppCompatActivity;

    import android.content.res.AssetManager;
    import android.graphics.Color;
    import android.graphics.Typeface;
    import android.os.Bundle;
    import android.view.View;
    import android.widget.Button;
    import android.widget.TextView;

    import java.io.IOException;
    import java.io.InputStream;

    public class MainActivity extends AppCompatActivity implements View.OnClickListener {

    private TextView textView;
    private Button colorButton;
    private Button fontButton;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        textView = findViewById(R.id.textView);
        colorButton = findViewById(R.id.colbut);
        fontButton = findViewById(R.id.fonbut);

        colorButton.setOnClickListener(this);
        fontButton.setOnClickListener(this);
    }

    @Override
    public void onClick(View view) {
        switch (view.getId()) {
            case R.id.colbut:
                changeTextColor();
                break;
            case R.id.fonbut:
                changeFont();
                break;
        }
    }

    private void changeTextColor() {
        int randomColor = generateRandomColor();
        textView.setTextColor(randomColor);
    }

    private void changeFont() {
        Typeface newFont = Typeface.createFromAsset(getAssets(), "font/pacifico.ttf");
        textView.setTypeface(newFont);
    }

    private int generateRandomColor() {
        int red = (int) (Math.random() * 256);
        int green = (int) (Math.random() * 256);
        int blue = (int) (Math.random() * 256);
        return Color.rgb(red, green, blue);
    }
    }


## OUTPUT
   ![xml](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/87f3a213-a6ca-4f4e-ab4f-50fb865588ac) <br>
   ![main](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/88157ada-0f43-4851-8377-833b8e4074a6) <br>
   ![crt](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/5a3239ed-ecfe-47bc-86e4-eecf45ea03ad) <br>
   ![strt](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/8757021d-ab85-4fe2-8cf6-9aeff41d7e52) <br>
   ![resum](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/69ccd14f-999b-4879-8436-8c6c05074048) <br>
   ![pas](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/55d07c84-8ebb-4bf4-ba22-fc649e8e14df) <br>
   ![stp](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/8989f4ba-f9d7-4003-ab59-53c44342f978) <br>
   ![res](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/1ac2fe13-042c-4824-bac1-9c0ff6088593) <br>
   ![des](https://github.com/HariHaranLK/Mobile-Application-Development/assets/132996089/b7fddcc8-e2ef-4c22-bcca-d92572cf143b) <br>

## RESULT
Thus a Simple Android Application create a HelloWorld Activity using all lifecycles methods to display messages using Android Studio is developed and executed successfully.
