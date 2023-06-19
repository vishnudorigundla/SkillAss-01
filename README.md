# SkillAss-02
Develop a program to create a Thread using Android Studio
## AIM:
Develop a program to perform a Thread using Android Studio

## EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

## ALGORITHM:

Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Thread Creation processing is done in MainActivity.java

Step 7: Save and run the application.

## Program:
## MainActivity.java:
```
package com.example.tc;
import android.os.Bundle;
import android.os.Handler;
import androidx.appcompat.app.AppCompatActivity;
import android.view.View;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {
    EditText edit_query;
    TextView textView;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        edit_query = findViewById(R.id.edit_query);
        textView = findViewById(R.id.text);
        findViewById(R.id.click).setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                runthread();
            }
        });
    }

    private void runthread() {
        final String s1 = edit_query.getText().toString();
        Handler handler = new Handler();
        handler.postDelayed(new Runnable() {
            @Override
            public void run() {
                runOnUiThread(new Runnable() {
                    @Override
                    public void run() {
                        textView.setText(s1);
                    }
                });
            }
        }, 5000);
    }
}
```
## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:gravity="center_horizontal"
    android:layout_marginTop="100dp"
    tools:context=".MainActivity">
    <EditText
        android:id="@+id/edit_query"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter string" />
    <Button
        android:id="@+id/click"
        android:layout_marginTop="50dp"
        style="@style/Base.TextAppearance.AppCompat.Widget.Button.Borderless.Colored"
        android:layout_width="wrap_content"
        android:background="#c1c1c1"
        android:textColor="#FFF"
        android:layout_height="wrap_content"
        android:text="Button" />
    <TextView
        android:id="@+id/text"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content" />
</LinearLayout>
```

## Output

![image](https://github.com/vishnudorigundla/SkillAss-01/assets/94175324/62ff4c38-6b69-427c-bf8a-24809c1045c8)

![WhatsApp Image 2023-06-15 at 20 45 29](https://github.com/Hemapriya-2004/SkillAss-01/assets/94184828/60d1fb23-7051-4665-8338-41c6d7ad22a6)

## Result:
Thus a Simple Android Creation to create an Thread synchronization using Android Studio was developed and executed successfully.

