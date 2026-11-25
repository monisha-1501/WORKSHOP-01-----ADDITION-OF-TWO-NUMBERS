# WORKSHOP-01-----ADDITION-OF-TWO-NUMBERS

## AIM:

To create an Android application to get two numbers from the user and display their sum in a text box using Android Studio.

## EQUIPMENTS REQUIRED:

  Android Studio (Minimum required: Arctic Fox), Java Programming Language, Android SDK, Computer/Laptop, Android Emulator or Android Mobile.

## ALGORITHM:

1. Open Android Studio and create a new project.

2. Design the user interface using XML.

3. Create two input fields to get two numbers.

4. Create an ADD button and a text box to display the result.

5. Write Java code to get the two input values.

6. Add the two numbers when the ADD button is clicked.

7. Display the sum in the text box.

8. Run the application and verify the output.

## PROGRAM:
```
/*
Program to print the text “Addition operation”.
Developed by: MONISHA D
Registeration Number : 212225240090
*/
```

#### MainActivity.java
```
package com.example.addition;

import android.os.Bundle;
import android.widget.*;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    EditText num1, num2;
    Button add;
    TextView result;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1 = findViewById(R.id.num1);
        num2 = findViewById(R.id.num2);
        add = findViewById(R.id.add);
        result = findViewById(R.id.result);

        add.setOnClickListener(v -> {
            int a = Integer.parseInt(num1.getText().toString());
            int b = Integer.parseInt(num2.getText().toString());

            int sum = a + b;

            result.setText("Sum = " + sum);
        });
    }
}
```

#### activity_main.xml
```
<LinearLayout
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/num1"
        android:hint="Enter first number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <EditText
        android:id="@+id/num2"
        android:hint="Enter second number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <Button
        android:id="@+id/add"
        android:text="ADD"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <TextView
        android:id="@+id/result"
        android:text="Result"
        android:textSize="22sp"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

</LinearLayout>
```

## OUTPUT
<img width="1915" height="1023" alt="Screenshot 2026-11-25 151119" src="https://github.com/user-attachments/assets/ab036d47-1016-4be7-af4c-616ab640a006" />

<img width="1917" height="1020" alt="Screenshot 2026-11-25 151142" src="https://github.com/user-attachments/assets/0e4c5b66-053e-4320-a12d-231080959069" />

<img width="1915" height="1023" alt="Screenshot 2026-11-25 151202" src="https://github.com/user-attachments/assets/d9b8039b-ec93-403b-a1fc-b2e8d1b772dc" />

## RESULT:

Thus, the Android application for adding two numbers was created and executed successfully using Android Studio.
