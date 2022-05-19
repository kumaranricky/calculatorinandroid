# Ex.No:7 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min.required Artic Fox)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:

/*
Program to print the text “calculator operation”.<br>
Developed by: Kumaran.B<br>
Registeration Number : 212220230026
*/





## activity_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/green"
    tools:context=".MainActivity">

    <Button
        android:id="@+id/button1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#E91E63"
        android:text="+"
        android:textSize="34sp"
        app:iconTint="#2196F3"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.113"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.471" />

    <EditText
        android:id="@+id/editTextNumber1"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="number"
        android:text="number 1"
        android:textAlignment="gravity"
        android:textColor="#673AB7"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.221" />

    <EditText
        android:id="@+id/editTextNumber2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:ems="10"
        android:inputType="number"
        android:text="number2"
        android:textColor="#9C27B0"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.497"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/editTextNumber1"
        app:layout_constraintVertical_bias="0.075" />

    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:background="#4CAF50"
        android:backgroundTint="#FF9800"
        android:text="-"
        android:textColor="#F44336"
        android:textSize="34sp"
        app:iconTint="#FF9800"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.802"
        app:layout_constraintStart_toEndOf="@+id/button1"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.471" />

    <Button
        android:id="@+id/button2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#FF5722"
        android:text="*"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        android:textColor="#3949AB"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toStartOf="@+id/button3"
        app:layout_constraintHorizontal_bias="0.222"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button1"
        app:layout_constraintVertical_bias="0.089" />

    <Button
        android:id="@+id/button3"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:backgroundTint="#FFB300"
        android:text="/"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        android:textColor="#43A047"
        app:iconTint="#FDD835"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.905"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button"
        app:layout_constraintVertical_bias="0.089" />

</androidx.constraintlayout.widget.ConstraintLayout>
```
## activity2_main.xml
```xml
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent">

    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_weight="1"
        android:text="The Solution  is:"
        android:textAppearance="@style/TextAppearance.AppCompat.Large"
        android:textColor="#E91E63"
        android:textColorHighlight="#4CAF50"
        android:textColorHint="@color/cardview_dark_background"
        android:textColorLink="#00BCD4"
        android:textSize="34sp"
        android:textStyle="bold"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.456"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.331" />

    <TextView
        android:id="@+id/textView2"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="TextView"
        android:textColor="#4CAF50"
        android:textSize="24sp"
        android:textStyle="italic"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.47"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/textView"
        app:layout_constraintVertical_bias="0.164" />
</androidx.constraintlayout.widget.ConstraintLayout>
```


## MainActivity.java
```java
package com.example.simplecalculator;

import androidx.appcompat.app.AppCompatActivity;

import android.content.Intent;
import android.os.Bundle;
import android.view.View;
import android.widget.EditText;
import android.widget.Button;

public class MainActivity extends AppCompatActivity {
    EditText num1text;
    EditText num2text;
    Button res,dif,mul,div;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        num1text=findViewById(R.id.editTextNumber1);
        num2text=findViewById(R.id.editTextNumber2);
        res=findViewById(R.id.button1);
        dif=findViewById(R.id.button);
        mul=findViewById(R.id.button2);
        div=findViewById(R.id.button3);
        res.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int num1=Integer.parseInt(num1text.getText().toString());
                int num2=Integer.parseInt(num2text.getText().toString());
                int sum=num1+num2;

                Intent i=new Intent(getApplicationContext(),MainActivity2.class);
                i.putExtra("Key",sum);
                startActivity(i);
            }
        });
        div.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int num1=Integer.parseInt(num1text.getText().toString());
                int num2=Integer.parseInt(num2text.getText().toString());
                int sum=num1/num2;

                Intent i=new Intent(getApplicationContext(),MainActivity2.class);
                i.putExtra("Key",sum);
                startActivity(i);
            }
        });
        dif.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int num1=Integer.parseInt(num1text.getText().toString());
                int num2=Integer.parseInt(num2text.getText().toString());
                int sum=num1-num2;

                Intent i=new Intent(getApplicationContext(),MainActivity2.class);
                i.putExtra("Key",sum);
                startActivity(i);
            }
        });
        mul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                int num1=Integer.parseInt(num1text.getText().toString());
                int num2=Integer.parseInt(num2text.getText().toString());
                int sum=num1*num2;

                Intent i=new Intent(getApplicationContext(),MainActivity2.class);
                i.putExtra("Key",sum);
                startActivity(i);
            }
        });
    }

}
```
## MainActivity2.java
```java
package com.example.simplecalculator;
import androidx.appcompat.app.AppCompatActivity;
import android.content.Intent;
import android.os.Bundle;
import android.widget.TextView;
public class MainActivity2 extends AppCompatActivity {
    TextView numText;
    int sum;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main2);
        numText = findViewById(R.id.textView2);
        Intent i = getIntent();
        sum = i.getIntExtra("Key", 0);
        numText.setText(Integer.toString(sum));

    }


}
```
## <br>OUTPUT
<br>
![Screenshot (197)](https://user-images.githubusercontent.com/75243072/169356848-a866bbbf-3b58-4102-aa8f-6874da74fd4d.png)<br>

![Screenshot (198)](https://user-images.githubusercontent.com/75243072/169356871-0a10634a-245c-4167-9dc0-1b7ffc6962dd.png)<br>

![Screenshot (199)](https://user-images.githubusercontent.com/75243072/169356890-f361259b-c1a3-4a42-9bd8-00b959046bfd.png)
![Scr!eenshot (200)](https://user-images.githubusercontent.com/75243072/169356910-45815ede-1bfa-41aa-8e1d-2a1fb1a86eb3.png)
![Screenshot (201)](https://user-images.githubusercontent.com/75243072/169356939-0835ac60-b0c4-480a-9aeb-0666006563d6.png)





## <br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/><br/>RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
