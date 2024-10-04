# Ex.No:1 Implementation of a Hello world Activity using all lifecycles methods using Android Studio.

# AIM:
To create Hello world Activity using all lifecycles methods to display messages using android studio.


# EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)


# ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as HelloWorld and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Display message give in MainActivity file.

Step 7: Save and run the application.


# PROGRAM:
```
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: Arya Baisakhiya
RegisterNumber: 212222040019
*/
```

# MainActivity.java:
```
package com.example.helloworld;

import android.os.Bundle;
import android.widget.Toast;
import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }

    @Override
    protected void onStart() {
        super.onStart();
        Toast.makeText(getApplicationContext(), "OnStart Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onResume() {
        super.onResume();
        Toast.makeText(getApplicationContext(), "OnResume Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onPause() {
        super.onPause();
        Toast.makeText(getApplicationContext(), "OnPause Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onStop() {
        super.onStop();
        Toast.makeText(getApplicationContext(), "OnStop Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onRestart() {
        super.onRestart();
        Toast.makeText(getApplicationContext(), "OnRestart Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Toast.makeText(getApplicationContext(), "OnDestroy Executed", Toast.LENGTH_LONG).show();
    }
}
```

# activitymain.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
# OUTPUT:
![img1](https://github.com/user-attachments/assets/36ecf4c6-d892-413f-80c2-fd6a10d0cbad)
![img2](https://github.com/user-attachments/assets/e5e2ef87-329b-4a90-9ac6-5f7c9c5d3933)
![img3](https://github.com/user-attachments/assets/ce5e55f6-014c-4c86-b4d5-a0d2dcac4050)
![img4](https://github.com/user-attachments/assets/a0621a02-734b-4a5b-b3e8-ecccef2665ee)
![img5](https://github.com/user-attachments/assets/1a03ab50-3ecb-42ac-a250-0f5c56cdd7f6)
![img6](https://github.com/user-attachments/assets/39a82a96-f298-4f70-b202-63e12a9c51fb)

# RESULT:
Thus a program to implement the various life cycles of an activity is written and successfully executed using Android Studio.
