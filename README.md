# Ex_6_Personal-Information-of-Student
Develop a program to accept personal information from the end user using Text View and Edit Text and display the information of the student.

## AIM:
To develop a program to accept personal information from the end user using Text View and Edit Text and display the information of the student using Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Min. required Artic Fox)


## ALGORITHM:
Step 1: Open Android Studio and then click on File -> New -> New project.

Step 2: Then type the Application name as SMSIntent and click Next.

Step 3: Select the Minimum SDK below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally, click Finish.

Step 5: Design layout in activity_main.xml.

Step 6: Accept the Personal Information from the User and display the information given in MainActivity.java

Step 7: Save and run the application.


## Program:
 ```
/*
Program to develop personal information for student
Developed by: Easwar J
RegisterNumber:  212221230024
*/
```

## MainActivity.java:
```

package com.example.ex_6;

import androidx.appcompat.app.AppCompatActivity;
//import android.support.v7.app.AppCompatActivity;
import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.Toast;
public class MainActivity extends AppCompatActivity {
    EditText name, dob, city, email, contact;
    Button submit;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        name = findViewById(R.id.name);
        dob = findViewById(R.id.dob);
        city = findViewById(R.id.city);
        email = findViewById(R.id.email);
        contact = findViewById(R.id.contact);
        submit = findViewById(R.id.btnSubmit);

        submit.setOnClickListener(new View.OnClickListener() {

            @Override
            public void onClick(View v) {

                String n = name.getText().toString();
                String d = dob.getText().toString();
                String ci = city.getText().toString();
                String e = email.getText().toString();
                String c = contact.getText().toString();

                if(n.isEmpty() || d.isEmpty() || ci.isEmpty() || e.isEmpty() || c.isEmpty())
                {
                    Toast.makeText(getApplicationContext(), "Please enter all data", Toast.LENGTH_SHORT).show();
                }
                else
                {
                    Toast.makeText(getApplicationContext(), n + "\n" + d + "\n" + ci + "\n" + e + "\n" + c, Toast.LENGTH_SHORT).show();
                }
            }
        });
    }
}
```

## activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity"
    android:padding="10dp"
    android:gravity="center">

    <TextView android:id="@+id/tvInfo"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:text="Personal Information of Student"
        android:textSize="20sp"
        android:gravity="center_horizontal"
        android:textStyle="bold"
        android:layout_marginTop="20dp"
        android:textColor="@android:color/holo_red_light"/>

    <EditText android:id="@+id/name"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter you name"
        android:ems="10"
        android:inputType="textPersonName"
        android:textSize="18sp"
        android:layout_marginTop="50dp"
        android:layout_below="@+id/tvInfo"/>

    <EditText android:id="@+id/dob"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Date of Birth"
        android:ems="10"
        android:inputType="date"
        android:textSize="18sp"
        android:layout_below="@+id/name"
        android:layout_marginTop="25dp"/>

    <EditText android:id="@+id/city"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter your City"
        android:ems="10"
        android:inputType="textCapCharacters"
        android:textSize="18sp"
        android:layout_below="@+id/dob"
        android:layout_marginTop="25dp"/>

    <EditText android:id="@+id/email"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Email ID"
        android:ems="10"
        android:inputType="textEmailAddress"
        android:textSize="18sp"
        android:layout_below="@+id/city"
        android:layout_marginTop="25dp"/>

    <EditText android:id="@+id/contact"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:hint="Enter Contact number"
        android:ems="10"
        android:inputType="date"
        android:textSize="18sp"
        android:layout_below="@+id/email"
        android:layout_marginTop="25dp"/>

    <Button android:id="@+id/btnSubmit"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_below="@id/contact"
        android:layout_marginTop="50dp"
        android:text="Submit"
        android:textSize="18sp"
        android:onClick="displayData"/>
</RelativeLayout>

```
## AndroidMainfest.xml
```
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools">

    <application
        android:allowBackup="true"
        android:dataExtractionRules="@xml/data_extraction_rules"
        android:fullBackupContent="@xml/backup_rules"
        android:icon="@mipmap/ic_launcher"
        android:label="@string/app_name"
        android:supportsRtl="true"
        android:theme="@style/Theme.Ex6"
        tools:targetApi="31">
        <activity
            android:name=".MainActivity"
            android:exported="true">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

</manifest>
```
## Output:

![output](https://github.com/jithendra2004/Ex_6_Personal-Information-of-Student/blob/main/6.png)


## Result:
Thus a Simple Android Application to create personal information from the end user and display the information of the student using Android Studio was developed and executed successfully.
