# **Addition App**

## **AIM**

To develop a simple Android application that accepts two numbers from the user and displays their sum.


## **ALGORITHM**

1. Open Android Studio and create a new project.
2. Create two EditText fields to enter two numbers.
3. Create an ADD button and a result EditText.
4. Get the values entered by the user.
5. Convert the values into integers.
6. Add the two numbers.
7. Display the sum in the result box.

## **PROGRAM**


ACTIVITY_MAIN.XML
```
<?xml version="1.0" encoding="utf-8"?>

<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="20dp">

    <EditText
        android:id="@+id/n1"
        android:hint="Enter first number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <EditText
        android:id="@+id/n2"
        android:hint="Enter second number"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <Button
        android:id="@+id/add"
        android:text="ADD"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

    <EditText
        android:id="@+id/result"
        android:hint="Result"
        android:inputType="number"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"/>

</LinearLayout>

```
MAINACTIVITY.JAVA
```
package com.example.addition;

import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;
import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        EditText n1 = findViewById(R.id.n1);
        EditText n2 = findViewById(R.id.n2);
        EditText result = findViewById(R.id.result);
        Button add = findViewById(R.id.add);

        add.setOnClickListener(v -> {
            int a = Integer.parseInt(n1.getText().toString());
            int b = Integer.parseInt(n2.getText().toString());
            result.setText(String.valueOf(a + b));
        });
    }
}



```
## **OUTPUT**

<img width="957" height="504" alt="Screenshot 2026-09-21 092714" src="https://github.com/user-attachments/assets/8b02ce9a-a858-4656-962d-3eee875462f5" />
<img width="959" height="506" alt="Screenshot 2026-09-21 092731" src="https://github.com/user-attachments/assets/8bfd96b5-849c-439f-ac6d-233521f4cdfc" />

## **RESULT**
Thus, the Android application was successfully developed to add two numbers and display the summation value.
