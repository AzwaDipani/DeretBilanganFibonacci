# DeretBilanganFibonacci

Nama : Muhammad Azwa Dipani

NIM : 312210417

Kelas : TI.22.A1

Mata Kuliah : Pemrograman Mobile 1

Tugas : Buatlah Method Program java Toast Number, dengan menghasilkan Bilangan Fibonacci

## Code pada menu program java class `(MainActivity.java)` :
```
package com.fibonaccisequence;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends AppCompatActivity {
    private int count = 1;
    private TextView showCount;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        showCount = findViewById(R.id.show_count);
    }

    public void showToast(View view) {
        Toast toast = Toast.makeText(this, "Hello Toast!", Toast.LENGTH_SHORT);
        toast.show();
    }

    public void countUp(View view) {
        if (count < 0) {
            count = 0;
        }

        int result = generateFibonacci(count);

        if (result <= 1000) {
            showCount.setText(Integer.toString(result));
            count++;
        }
    }

    private int generateFibonacci(int n) {
        if (n <= 0) {
            return 0;
        } else if (n == 1) {
            return 1;
        }

        int first = 0;
        int second = 1;

        for (int i = 2; i <= n; i++) {
            int next = first + second;
            first = second;
            second = next;
        }

        return second;
    }

    public void Reset(View view) {
        count = 1;
        showCount.setText("1");
    }

}
```

## Code pada menu layout (activity_main.xml) :
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">


    <Button
        android:id="@+id/button_toast"
        android:layout_width="421dp"
        android:layout_height="48dp"
        android:background="@color/colorPrimary"
        android:onClick="showToast"
        android:text="Toast"
        android:textColor="@android:color/white"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <Button
        android:id="@+id/button2"
        android:layout_width="205dp"
        android:layout_height="46dp"
        android:background="@color/colorPrimary"
        android:onClick="countUp"
        android:text="@string/button_label_count"
        android:textColor="@android:color/white"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/show_count"
        android:layout_width="411dp"
        android:layout_height="636dp"
        android:background="#FFFF00"
        android:gravity="center_vertical"
        android:text="1"
        android:textAlignment="center"
        android:textColor="@color/colorPrimary"
        android:textSize="160dp"
        android:textStyle="bold"
        app:layout_constraintBottom_toTopOf="@+id/button2"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.571"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button_toast"
        app:layout_constraintVertical_bias="0.0"
        tools:ignore=",Rtlcompat" />

    <Button
        android:id="@+id/button"
        android:layout_width="202dp"
        android:layout_height="49dp"
        android:background="@color/colorPrimary"
        android:onClick="Reset"
        android:text="Back"
        android:textColor="@android:color/white"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="1.0"
        app:layout_constraintStart_toEndOf="@+id/button2"
        app:layout_constraintTop_toBottomOf="@+id/show_count"
        app:layout_constraintVertical_bias="0.0" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

## Code pada menu values (strings.xml) :
```
<resources>
    <string name="app_name">FibonacciSequence</string>
    <string name="button_label_toast">Toast</string>
    <string name="button_label_count">Count</string>
    <string name="count_initial_value">0</string>
    <string name="coast_message">Hello Toast</string>
    <string name="Reset">Reset</string>
</resources>
```

## Code pada menu values (colors.xml) :
```
<?xml version="1.0" encoding="utf-8"?>
<resources>
    <color name="black">#FF000000</color>
    <color name="white">#FFFFFFFF</color>
    <color name="blue">#3700B3</color>
    <color name="pink">#FFC0CB</color>
    <color name="colorPrimary">#3F5185</color>
    <color name="colorPrimaryDark">#303F9F</color>
    <color name="colorAccent">#FF4081</color>
</resources>
```


## Hasil run program bilangan Fibonacci :






https://github.com/AzwaDipani/DeretBilanganFibonacci/assets/115677539/1c19689c-9938-405e-bd51-e0a7a79fa5f9







## Finish, Terima Kasih
